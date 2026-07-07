---
layout: post
title: "systemd unit failed after dnf upgrade"
date: 2026-07-07 09:00:00 +0530
categories: [linux, devops, systemd]
author: Satish Mane
---

A custom service stopped starting after a Fedora `dnf upgrade` — the binary path had moved and the systemd unit file was still pointing to the old location.

## Problem

After upgrading packages on Fedora with `dnf upgrade`, a custom app service refused to start. `journalctl` showed:

```
Failed to start myapp.service - My Application.
```

No other useful error — just a failed status.

## Solution

The unit file still referenced the old binary path `/usr/local/bin/myapp` but `dnf` moved the binary to `/usr/bin/myapp` during the upgrade. Updated `ExecStart` in the unit file to point to the correct path.

### Commands

```bash
# Check what's actually failing
systemctl status myapp.service
journalctl -u myapp.service -b --no-pager

# Find where the binary actually lives now
which myapp

# Fix the unit file (update ExecStart path)
sudo vim /etc/systemd/system/myapp.service

# Reload and restart
systemctl daemon-reload && systemctl restart myapp.service
```

## Why this happens

When `dnf` upgrades a package, the new version may install the binary to a different prefix — typically moving from `/usr/local/bin` to `/usr/bin` (or vice versa). If you wrote a custom systemd unit file with a hardcoded `ExecStart` path, that path goes stale after the upgrade. systemd doesn't resolve `$PATH` — it needs the absolute path to the binary.

This is especially common on Fedora where packages move between `/usr/sbin` and `/usr/bin` as part of the [UsrMerge](https://fedoraproject.org/wiki/Changes/Unify_Usr_Bin) effort.

## Takeaways

- Always check `which <binary>` or `rpm -ql <package>` after an upgrade to confirm the install path
- Use `ExecStart=` with the output of `which` rather than assuming a path
- Run `systemctl daemon-reload` after editing any unit file — systemd caches unit definitions in memory
