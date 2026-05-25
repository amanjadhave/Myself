<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aman Jadhave — GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  :root {
    --bg: #0d1117;
    --bg2: #161b22;
    --bg3: #1c2128;
    --border: #30363d;
    --accent: #58a6ff;
    --green: #3fb950;
    --amber: #d29922;
    --red: #f85149;
    --text: #e6edf3;
    --muted: #7d8590;
    --mono: 'JetBrains Mono', monospace;
    --display: 'Syne', sans-serif;
  }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--mono);
    font-size: 14px;
    line-height: 1.6;
    padding: 2.5rem 1.5rem;
    max-width: 880px;
    margin: 0 auto;
  }

  /* ── TERMINAL CHROME ── */
  .terminal-bar {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 10px 10px 0 0;
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot.r { background: var(--red); }
  .dot.y { background: var(--amber); }
  .dot.g { background: var(--green); }
  .terminal-label { font-size: 12px; color: var(--muted); margin-left: auto; }

  .terminal-body {
    background: var(--bg);
    border: 1px solid var(--border);
    border-top: none;
    border-radius: 0 0 10px 10px;
    padding: 2rem 2rem 2.5rem;
  }

  .prompt { color: var(--green); font-weight: 700; }
  .cmd    { color: var(--accent); }
  .cursor {
    display: inline-block; width: 8px; height: 16px;
    background: var(--accent);
    animation: blink 1.2s step-end infinite;
    vertical-align: text-bottom;
  }
  @keyframes blink { 50% { opacity: 0; } }

  /* ── NAME BLOCK ── */
  .name-block {
    margin: 2rem 0 1rem;
    border-left: 3px solid var(--accent);
    padding-left: 1.2rem;
  }
  .name-big {
    font-family: var(--display);
    font-size: 2rem;
    font-weight: 800;
    color: var(--text);
    letter-spacing: -0.5px;
    line-height: 1.2;
  }
  .name-big span { color: var(--accent); }
  .name-role {
    font-size: 13px;
    color: var(--muted);
    margin-top: 6px;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }

  /* ── BADGES ── */
  .badge-row { display: flex; flex-wrap: wrap; gap: 8px; margin: 1.25rem 0; }
  .badge {
    font-size: 11px;
    font-family: var(--mono);
    padding: 3px 10px;
    border-radius: 20px;
    border: 1px solid;
    font-weight: 500;
  }
  .badge.blue   { color: #58a6ff; border-color: #58a6ff40; background: #58a6ff12; }
  .badge.green  { color: #3fb950; border-color: #3fb95040; background: #3fb95012; }
  .badge.amber  { color: #d29922; border-color: #d2992240; background: #d2992212; }
  .badge.purple { color: #bc8cff; border-color: #bc8cff40; background: #bc8cff12; }

  /* ── SECTION TITLE ── */
  .section-title {
    font-family: var(--display);
    font-size: 11px;
    font-weight: 700;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 2px;
    margin: 2rem 0 1rem;
  }

  /* ── CARDS ── */
  .card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1rem 1.25rem;
    margin-bottom: 10px;
    transition: border-color 0.2s;
  }
  .card:hover { border-color: var(--accent); }
  .card-header { display: flex; align-items: center; gap: 10px; margin-bottom: 6px; }
  .card-icon  { color: var(--accent); font-size: 14px; }
  .card-title { font-weight: 600; font-size: 13.5px; color: var(--text); }
  .card-meta  { font-size: 11px; color: var(--muted); margin-left: auto; }
  .card-desc  { font-size: 12.5px; color: var(--muted); padding-left: 24px; }

  .grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  @media (max-width: 560px) { .grid2 { grid-template-columns: 1fr; } }

  /* ── SKILLS ── */
  .skill-group  { margin-bottom: 1rem; }
  .skill-label  { font-size: 11px; color: var(--muted); margin-bottom: 6px; text-transform: uppercase; letter-spacing: 1px; }
  .skill-tags   { display: flex; flex-wrap: wrap; gap: 6px; }
  .skill-tag {
    font-size: 11px;
    background: var(--bg3);
    border: 1px solid var(--border);
    color: var(--text);
    padding: 3px 10px;
    border-radius: 4px;
  }

  /* ── CAREER PATH ── */
  .path-row {
    display: flex;
    align-items: center;
    gap: 0;
    margin: 1rem 0;
    flex-wrap: wrap;
    gap: 6px;
  }
  .path-step {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 8px 14px;
    font-size: 12px;
    white-space: nowrap;
  }
  .path-step.current { border-color: var(--green); color: var(--green); }
  .path-step.next    { border-color: var(--accent); color: var(--accent); }
  .path-step.future  { color: var(--muted); }
  .path-arrow        { color: var(--muted); font-size: 14px; }

  /* ── DIVIDER ── */
  .divider { border: none; border-top: 1px solid var(--border); margin: 1.5rem 0; }

  /* ── LEARNING BOX ── */
  .learning-box {
    font-size: 13px;
    color: var(--muted);
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1rem 1.25rem;
    line-height: 2;
  }
  .learning-box span { color: var(--green); }

  /* ── CONNECT ── */
  .connect-row { display: flex; align-items: center; gap: 12px; flex-wrap: wrap; margin-top: 1.5rem; }
  .connect-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 12px;
    color: var(--accent);
    text-decoration: none;
    border: 1px solid #58a6ff40;
    background: #58a6ff08;
    border-radius: 6px;
    padding: 6px 14px;
    transition: background 0.2s;
  }
  .connect-link:hover { background: #58a6ff22; }
  .connect-dot {
    width: 6px; height: 6px; border-radius: 50%;
    background: var(--green);
    animation: blink 2s ease-in-out infinite;
    display: inline-block;
  }

  /* ── FOOTER ── */
  .footer-note {
    font-size: 11px;
    color: var(--muted);
    margin-top: 2rem;
    padding-top: 1rem;
    border-top: 1px solid var(--border);
  }
  code {
    background: var(--bg3);
    border: 1px solid var(--border);
    border-radius: 3px;
    padding: 1px 5px;
    font-size: 12px;
    color: #ff7b72;
  }

  /* ── COPY BUTTON ── */
  #copy-btn {
    display: block;
    margin: 1.5rem auto 0;
    font-family: var(--mono);
    font-size: 13px;
    background: var(--bg2);
    color: var(--accent);
    border: 1px solid #58a6ff40;
    border-radius: 6px;
    padding: 8px 22px;
    cursor: pointer;
    transition: background 0.2s;
  }
  #copy-btn:hover { background: #58a6ff18; }
</style>
</head>
<body>

<div class="terminal-bar">
  <div class="dot r"></div>
  <div class="dot y"></div>
  <div class="dot g"></div>
  <span class="terminal-label">amanjadhave / README.md</span>
</div>

<div class="terminal-body">

  <!-- PROMPT -->
  <div style="margin-bottom:14px">
    <span class="prompt">visitor@github:~$</span> <span class="cmd">cat profile.md</span>
  </div>

  <!-- NAME -->
  <div class="name-block">
    <div class="name-big">Aman <span>Jadhave</span></div>
    <div class="name-role">Desktop Support Engineer → System Administrator</div>
  </div>

  <!-- BADGES -->
  <div class="badge-row">
    <span class="badge green">● Open to Work</span>
    <span class="badge blue">Desktop Support</span>
    <span class="badge blue">Windows Environments</span>
    <span class="badge amber">Networking</span>
    <span class="badge purple">Learning Linux &amp; PowerShell</span>
    <span class="badge amber">Learning Azure</span>
  </div>

  <!-- BIO -->
  <div style="font-size:13px; color:var(--muted); line-height:1.8; max-width:640px;">
    IT Support engineer with hands-on experience delivering Level 1 helpdesk support —
    diagnosing hardware/software faults, managing endpoints, configuring LAN/Wi-Fi, and
    providing remote assistance. Building toward a Sysadmin role with active study of
    Linux, PowerShell scripting, and cloud fundamentals.
  </div>

  <hr class="divider">

  <!-- CAREER PATH -->
  <div class="section-title">⬡ Career Path</div>
  <div class="path-row">
    <div class="path-step current">✓ Tier 1 Helpdesk</div>
    <span class="path-arrow">──▶</span>
    <div class="path-step next">⟳ Tier 2 / Desktop Support</div>
    <span class="path-arrow">──▶</span>
    <div class="path-step future">◯ Sysadmin / SysEng</div>
    <span class="path-arrow">──▶</span>
    <div class="path-step future">◯ Cloud / DevOps</div>
  </div>

  <hr class="divider">

  <!-- SKILLS -->
  <div class="section-title">⬡ Technical Stack</div>

  <div class="skill-group">
    <div class="skill-label">Operating Systems</div>
    <div class="skill-tags">
      <span class="skill-tag">Windows 10/11</span>
      <span class="skill-tag">Windows Server (Basic)</span>
      <span class="skill-tag">Linux (Learning)</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="skill-label">Networking</div>
    <div class="skill-tags">
      <span class="skill-tag">TCP/IP</span>
      <span class="skill-tag">DNS / DHCP</span>
      <span class="skill-tag">LAN / WAN</span>
      <span class="skill-tag">VPN</span>
      <span class="skill-tag">Wi-Fi Troubleshooting</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="skill-label">Remote &amp; Support Tools</div>
    <div class="skill-tags">
      <span class="skill-tag">AnyDesk</span>
      <span class="skill-tag">TeamViewer</span>
      <span class="skill-tag">RDP</span>
      <span class="skill-tag">Ticketing Systems</span>
      <span class="skill-tag">Antivirus / Endpoint</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="skill-label">Hardware</div>
    <div class="skill-tags">
      <span class="skill-tag">Desktop / Laptop Repair</span>
      <span class="skill-tag">RAM / SSD Upgrade</span>
      <span class="skill-tag">BIOS Config</span>
      <span class="skill-tag">Printer Setup</span>
      <span class="skill-tag">Preventive Maintenance</span>
    </div>
  </div>

  <div class="skill-group">
    <div class="skill-label">Scripting &amp; Cloud (In Progress)</div>
    <div class="skill-tags">
      <span class="skill-tag" style="border-style:dashed;">PowerShell ⟳</span>
      <span class="skill-tag" style="border-style:dashed;">Azure Fundamentals ⟳</span>
      <span class="skill-tag" style="border-style:dashed;">Bash / Linux CLI ⟳</span>
    </div>
  </div>

  <hr class="divider">

  <!-- PROJECTS -->
  <div class="section-title">⬡ Featured Projects</div>
  <div class="grid2">

    <div class="card">
      <div class="card-header">
        <span class="card-icon">⬡</span>
        <span class="card-title">Windows OS Deployment</span>
        <span class="card-meta badge blue">Windows</span>
      </div>
      <div class="card-desc">
        Deployed &amp; standardized Win 10/11 on multiple machines — drivers, MS Office, AV, and security patches.
      </div>
    </div>

    <div class="card">
      <div class="card-header">
        <span class="card-icon">⬡</span>
        <span class="card-title">Office Network Setup</span>
        <span class="card-meta badge amber">Networking</span>
      </div>
      <div class="card-desc">
        Configured LAN/Wi-Fi, IP addressing; resolved DNS and printer-sharing issues across office devices.
      </div>
    </div>

    <div class="card">
      <div class="card-header">
        <span class="card-icon">⬡</span>
        <span class="card-title">Hardware Upgrades</span>
        <span class="card-meta badge green">Hardware</span>
      </div>
      <div class="card-desc">
        RAM &amp; SSD upgrades, faulty component diagnostics, and scheduled preventive maintenance.
      </div>
    </div>

    <div class="card">
      <div class="card-header">
        <span class="card-icon">⬡</span>
        <span class="card-title">Remote IT Support</span>
        <span class="card-meta badge purple">Tools</span>
      </div>
      <div class="card-desc">
        Delivered L1 remote support via AnyDesk &amp; TeamViewer — ticket management and system updates.
      </div>
    </div>

  </div>

  <hr class="divider">

  <!-- CERTS & EDUCATION -->
  <div class="section-title">⬡ Certifications &amp; Education</div>

  <div class="card">
    <div class="card-header">
      <span class="card-icon">✓</span>
      <span class="card-title">Desktop Support Engineer Internship</span>
      <span class="card-meta">Interninfotech, Indore</span>
    </div>
  </div>

  <div class="card">
    <div class="card-header">
      <span class="card-icon">✓</span>
      <span class="card-title">B.Com (Computer Applications)</span>
      <span class="card-meta">DAVV University · 2022 · 88.15%</span>
    </div>
  </div>

  <hr class="divider">

  <!-- CURRENTLY LEARNING -->
  <div class="section-title">⬡ Currently Learning</div>
  <div class="learning-box">
    <span>→</span> Linux command line &amp; file system navigation<br>
    <span>→</span> PowerShell scripting for IT automation<br>
    <span>→</span> Microsoft Azure (AZ-900 fundamentals)<br>
    <span>→</span> Active Directory &amp; Group Policy basics
  </div>

  <!-- CONNECT -->
  <div class="connect-row">
    <div>
      <div class="connect-dot"></div>
      <span style="font-size:12px; color:var(--muted); margin-left:6px;">Open to opportunities in Indore &amp; remote</span>
    </div>
    <a class="connect-link" href="https://www.linkedin.com/in/aman-jadhave/" target="_blank">↗ LinkedIn</a>
    <a class="connect-link" href="mailto:amanjadhave.work@gmail.com">↗ Email</a>
  </div>

  <!-- FOOTER -->
  <div class="footer-note">
    <span class="cursor"></span>&nbsp;
    <code>feel free to connect</code> · <code>always learning</code> · <code>indore, india</code>
  </div>

</div>

<button id="copy-btn" onclick="copyHTML()">⬡ Copy Full HTML</button>

<script>
  function copyHTML() {
    const html = document.documentElement.outerHTML;
    navigator.clipboard.writeText(html).then(() => {
      const btn = document.getElementById('copy-btn');
      btn.textContent = '✓ Copied!';
      setTimeout(() => btn.textContent = '⬡ Copy Full HTML', 2000);
    });
  }
</script>

</body>
</html>
