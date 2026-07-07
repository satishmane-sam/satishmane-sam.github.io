---
layout: home
title: Home
---

<section class="hero">
  <div class="hero-grid">
    <div class="hero-main">
      <p class="hero-eyebrow">Linux · DevOps · Sysadmin</p>
      <h1 class="hero-title">Satish Mane</h1>
      <p class="hero-tagline">Small tools, real fixes, no fluff.</p>
      <p class="hero-intro">
        Practical notes from the terminal — systemd failures, Kubernetes quirks,
        Fedora/RHEL upgrades, and the CLI tools that save hours when production
        is on fire.
      </p>
      <div class="hero-actions">
        <a class="btn btn-primary" href="#posts">Read the blog</a>
        <a class="btn btn-ghost" href="https://github.com/satishmane-sam">GitHub</a>
        <a class="btn btn-ghost" href="/about/">About</a>
      </div>
      <ul class="hero-tags">
        <li>Linux</li>
        <li>DevOps</li>
        <li>Kubernetes</li>
        <li>systemd</li>
        <li>Fedora</li>
        <li>Ansible</li>
      </ul>
    </div>
    <aside class="hero-terminal" aria-label="Terminal preview">
      <div class="terminal-bar">
        <span></span><span></span><span></span>
        <p>satish@fedora ~</p>
      </div>
      <pre class="terminal-body"><code>$ preflight --json
<span class="t-ok">✓</span> disk_root      <span class="t-dim">/</span> 77% used
<span class="t-ok">✓</span> systemd_failed <span class="t-dim">no failed units</span>
<span class="t-ok">✓</span> dns            <span class="t-dim">github.com resolves</span>
<span class="t-ok">✓</span> kube_context   <span class="t-dim">context set</span>

<span class="t-prompt">$</span> journalctl -u myapp -b --no-pager
<span class="t-warn">→</span> ExecStart path wrong after dnf upgrade
<span class="t-prompt">$</span> systemctl daemon-reload && systemctl restart myapp
<span class="t-ok">→ fixed. writing it up...</span></code></pre>
    </aside>
  </div>
</section>

<section class="highlights">
  <article class="highlight-card">
    <span class="card-icon">🔧</span>
    <h2>Build</h2>
    <p>Open-source CLI tools and scripts for real production problems.</p>
  </article>
  <article class="highlight-card">
    <span class="card-icon">📝</span>
    <h2>Write</h2>
    <p>Clear write-ups when something breaks — commands, context, and the fix.</p>
  </article>
  <article class="highlight-card">
    <span class="card-icon">🚀</span>
    <h2>Ship</h2>
    <p>Preflight checks, automated workflows, and lessons from the field.</p>
  </article>
</section>

<section class="topics-strip">
  <h2>What I write about</h2>
  <div class="topics-grid">
    <div class="topic-item">
      <strong>systemd & services</strong>
      <span>Unit files, journalctl, daemon-reload</span>
    </div>
    <div class="topic-item">
      <strong>Kubernetes & containers</strong>
      <span>Clusters, contexts, deploy workflows</span>
    </div>
    <div class="topic-item">
      <strong>Fedora / RHEL</strong>
      <span>dnf upgrades, package moves, SELinux</span>
    </div>
    <div class="topic-item">
      <strong>Automation</strong>
      <span>Ansible, scripts, CI pipelines</span>
    </div>
  </div>
</section>

<section class="about-strip">
  <h2>About this blog</h2>
  <p>
    This is my personal lab notebook — not a news aggregator. Every post comes from
    actual work: a service that wouldn't start, a cluster that behaved oddly, or a
    one-liner that saved a Friday night. Copy the commands, skip the fluff.
  </p>
</section>
