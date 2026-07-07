---
layout: post
title: "systemd unit failed after dnf upgrade"
date: 2026-07-07 09:00:00 +0530
categories: [linux, devops, systemd]
author: Satish Mane
---

> Linux & DevOps — small tools, real fixes, no fluff.

## Problem

After upgrading packages on Fedora, a custom app service would not start. journalctl showed "Failed to start" with no obvious error.
## Solution

The unit file still referenced an old binary path under /usr/local/bin after the package moved to /usr/bin. Updated ExecStart and ran daemon-reload.
### Commands

```bash
systemctl daemon-reload && systemctl restart myapp.service
journalctl -u myapp.service -b --no-pager
```

## Why this happens

Explain the root cause in plain language. Link to man pages or docs if helpful.

## Takeaways

- Bullet 1 (edit me)
- Bullet 2 (edit me)
- Bullet 3 (edit me)
