---
layout: home
title: ""
---

<section class="hero-section">
  <h2 class="article-title">About Me</h2>
  <div class="hero-text">
    <p>
      Linux & DevOps practitioner writing about real infrastructure work — not theory.
      Practical notes from the terminal: systemd failures, Kubernetes quirks,
      Fedora/RHEL upgrades, and the CLI tools that save hours when production is on fire.
    </p>
  </div>
  <div class="hero-tags">
    <span class="hero-tag">Linux</span>
    <span class="hero-tag">DevOps</span>
    <span class="hero-tag">Kubernetes</span>
    <span class="hero-tag">systemd</span>
    <span class="hero-tag">Fedora</span>
    <span class="hero-tag">Ansible</span>
  </div>
</section>

<section class="service">
  <h2 class="article-title">What I Do</h2>
  <div class="service-list">
    <div class="service-item">
      <span class="service-icon">🔧</span>
      <div class="service-content-box">
        <h4 class="service-item-title"><a href="https://github.com/satishmane-sam" style="color:inherit">Build</a></h4>
        <p class="service-item-text">Open-source CLI tools and scripts for real production problems.</p>
      </div>
    </div>
    <div class="service-item">
      <span class="service-icon">📝</span>
      <div class="service-content-box">
        <h4 class="service-item-title"><a href="#posts" style="color:inherit">Write</a></h4>
        <p class="service-item-text">Clear write-ups when something breaks — commands, context, and the fix.</p>
      </div>
    </div>
    <div class="service-item">
      <span class="service-icon">🚀</span>
      <div class="service-content-box">
        <h4 class="service-item-title"><a href="/about/" style="color:inherit">Ship</a></h4>
        <p class="service-item-text">Preflight checks, automated workflows, and lessons from the field.</p>
      </div>
    </div>
  </div>
</section>

<section class="topics-section">
  <h2 class="article-title">Topics I Cover</h2>
  <div class="topics-grid">
    <div class="topic-card">
      <strong>systemd & services</strong>
      <span>Unit files, journalctl, daemon-reload</span>
    </div>
    <div class="topic-card">
      <strong>Kubernetes & containers</strong>
      <span>Clusters, contexts, deploy workflows</span>
    </div>
    <div class="topic-card">
      <strong>Fedora / RHEL</strong>
      <span>dnf upgrades, package moves, SELinux</span>
    </div>
    <div class="topic-card">
      <strong>Automation</strong>
      <span>Ansible, scripts, CI pipelines</span>
    </div>
  </div>
</section>

<section class="terminal-section">
  <h2 class="article-title">From The Terminal</h2>
  <div class="hero-terminal">
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
  </div>
</section>

<section class="about-strip">
  <h2>About This Blog</h2>
  <p>
    This is my personal lab notebook — not a news aggregator. Every post comes from
    actual work: a service that wouldn't start, a cluster that behaved oddly, or a
    one-liner that saved a Friday night. Copy the commands, skip the fluff.
  </p>
</section>
