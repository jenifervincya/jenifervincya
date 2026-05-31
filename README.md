
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=DM+Sans:wght@300;400;500;600&display=swap');
  *{box-sizing:border-box;margin:0;padding:0}
  :root{
    --accent:#5B8AF5;
    --accent2:#38E8C5;
    --dim:#8892b0;
    --card-bg:rgba(13,20,40,0.85);
    --border:rgba(91,138,245,0.18);
    --text:#CDD9FF;
    --head:#E8F0FF;
  }
  body{background:#060D1F;font-family:'DM Sans',sans-serif;color:var(--text);padding:0}
  .wrap{max-width:800px;margin:0 auto;padding:2rem 1.5rem 3rem}
  .hero{text-align:center;padding:2.5rem 0 2rem;position:relative}
  .hero-tag{font-family:'Space Mono',monospace;font-size:11px;color:var(--accent2);letter-spacing:3px;text-transform:uppercase;margin-bottom:1rem;opacity:0.9}
  .hero-name{font-size:clamp(2rem,5vw,3.2rem);font-weight:600;color:var(--head);letter-spacing:-1px;line-height:1.1;margin-bottom:0.6rem}
  .hero-name span{background:linear-gradient(120deg,#5B8AF5,#38E8C5);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
  .hero-sub{font-size:14px;color:var(--dim);font-family:'Space Mono',monospace;margin-bottom:1.8rem;letter-spacing:0.5px}
  .badges{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-bottom:2rem}
  .badge{padding:5px 14px;border-radius:20px;font-size:12px;font-family:'Space Mono',monospace;letter-spacing:0.5px;border:1px solid}
  .badge-blue{background:rgba(91,138,245,0.1);border-color:rgba(91,138,245,0.3);color:#7FAAFF}
  .badge-teal{background:rgba(56,232,197,0.1);border-color:rgba(56,232,197,0.3);color:#38E8C5}
  .badge-gray{background:rgba(255,255,255,0.04);border-color:rgba(255,255,255,0.1);color:var(--dim)}
  .links{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-bottom:2.5rem}
  .link-btn{display:flex;align-items:center;gap:6px;padding:7px 16px;border-radius:8px;font-size:12px;font-family:'Space Mono',monospace;text-decoration:none;border:1px solid;transition:all .2s;cursor:pointer}
  .link-btn:hover{transform:translateY(-2px)}
  .link-li{background:rgba(10,102,194,0.12);border-color:rgba(10,102,194,0.3);color:#6BAAD4}
  .link-gh{background:rgba(255,255,255,0.05);border-color:rgba(255,255,255,0.12);color:#CDD9FF}
  .link-gm{background:rgba(234,67,53,0.1);border-color:rgba(234,67,53,0.25);color:#E8806E}
  .section-label{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:3px;text-transform:uppercase;color:var(--accent);margin-bottom:1rem;display:flex;align-items:center;gap:10px}
  .section-label::after{content:'';flex:1;height:1px;background:var(--border)}
  .stats-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:10px;margin-bottom:2.5rem}
  .stat-card{background:var(--card-bg);border:1px solid var(--border);border-radius:10px;padding:1rem;text-align:center;backdrop-filter:blur(4px)}
  .stat-val{font-family:'Space Mono',monospace;font-size:1.5rem;font-weight:700;color:var(--head);display:block;line-height:1}
  .stat-lbl{font-size:11px;color:var(--dim);margin-top:5px;line-height:1.4}
  .stat-ico{font-size:18px;margin-bottom:6px}
  .projects{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:2.5rem}
  .proj-card{background:var(--card-bg);border:1px solid var(--border);border-radius:12px;padding:1.2rem;position:relative;overflow:hidden;transition:border-color .2s}
  .proj-card:hover{border-color:rgba(91,138,245,0.4)}
  .proj-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--accent),var(--accent2))}
  .proj-name{font-size:14px;font-weight:600;color:var(--head);margin-bottom:4px;font-family:'Space Mono',monospace}
  .proj-desc{font-size:12px;color:var(--dim);margin-bottom:10px;line-height:1.5}
  .proj-tags{display:flex;flex-wrap:wrap;gap:5px}
  .tag{font-size:10px;font-family:'Space Mono',monospace;padding:2px 8px;border-radius:4px;background:rgba(91,138,245,0.1);color:var(--accent);border:1px solid rgba(91,138,245,0.2)}
  .tag-t{background:rgba(56,232,197,0.08);color:var(--accent2);border-color:rgba(56,232,197,0.2)}
  .stack-section{margin-bottom:2.5rem}
  .stack-row{margin-bottom:14px}
  .stack-lbl{font-size:12px;color:var(--dim);margin-bottom:7px;font-family:'Space Mono',monospace}
  .pills{display:flex;flex-wrap:wrap;gap:7px}
  .pill{font-size:11px;padding:4px 12px;border-radius:5px;background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.09);color:var(--text);font-family:'Space Mono',monospace}
  .pill-hi{background:rgba(91,138,245,0.09);border-color:rgba(91,138,245,0.2);color:#7FAAFF}
  .exp-item{background:var(--card-bg);border:1px solid var(--border);border-radius:10px;padding:1rem 1.2rem;margin-bottom:10px;display:flex;gap:14px;align-items:flex-start}
  .exp-dot{width:34px;height:34px;border-radius:8px;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:16px;margin-top:2px}
  .dot-blue{background:rgba(91,138,245,0.12);border:1px solid rgba(91,138,245,0.2)}
  .dot-teal{background:rgba(56,232,197,0.1);border:1px solid rgba(56,232,197,0.2)}
  .dot-amber{background:rgba(250,199,117,0.1);border:1px solid rgba(250,199,117,0.2)}
  .exp-role{font-size:13px;font-weight:600;color:var(--head);margin-bottom:2px}
  .exp-org{font-size:12px;color:var(--accent);font-family:'Space Mono',monospace;margin-bottom:4px}
  .exp-pts{font-size:11px;color:var(--dim);line-height:1.7}
  .ach-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:2.5rem}
  .ach-item{background:rgba(91,138,245,0.04);border:1px solid var(--border);border-radius:8px;padding:9px 12px;font-size:12px;color:var(--text);display:flex;align-items:center;gap:8px}
  .ach-dot{width:6px;height:6px;border-radius:50%;background:var(--accent2);flex-shrink:0}
  .cert-cols{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:2.5rem}
  .cert-group{background:var(--card-bg);border:1px solid var(--border);border-radius:10px;padding:1rem}
  .cert-title{font-size:11px;font-family:'Space Mono',monospace;color:var(--accent);letter-spacing:1px;margin-bottom:10px}
  .cert-item{font-size:12px;color:var(--dim);padding:4px 0;border-bottom:1px solid rgba(255,255,255,0.04);line-height:1.4;display:flex;align-items:center;gap:7px}
  .cert-item:last-child{border-bottom:none}
  .cert-check{color:var(--accent2);font-size:14px;flex-shrink:0}
  .learn-grid{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:2.5rem}
  .learn-item{background:rgba(56,232,197,0.06);border:1px solid rgba(56,232,197,0.15);border-radius:6px;padding:6px 13px;font-size:12px;color:var(--accent2);font-family:'Space Mono',monospace}
  .footer{text-align:center;padding:2rem 0 0;border-top:1px solid var(--border)}
  .footer-quote{font-family:'Space Mono',monospace;font-size:12px;color:var(--dim);letter-spacing:1px}
  .footer-quote span{color:var(--accent2)}
  .ieee{display:inline-flex;align-items:center;gap:8px;margin-top:1.5rem;background:rgba(91,138,245,0.07);border:1px solid rgba(91,138,245,0.2);border-radius:8px;padding:8px 16px;font-size:12px;font-family:'Space Mono',monospace;color:#7FAAFF}
  @media(max-width:560px){.projects,.cert-cols,.ach-grid{grid-template-columns:1fr}.links{gap:7px}}
</style>

<div class="wrap">

  <div class="hero">
    <div class="hero-tag">// Embedded Systems Engineer</div>
    <div class="hero-name">Jenifer <span>Vincy</span> A</div>
    <div class="hero-sub">STM32 · ESP32 · Industrial IoT · Edge AI · PCB Design</div>
    <div class="badges">
      <span class="badge badge-blue">EEE Undergraduate</span>
      <span class="badge badge-teal">CGPA 8.79</span>
      <span class="badge badge-blue">IEEE Member</span>
      <span class="badge badge-gray">SIH 2025 Finalist</span>
      <span class="badge badge-teal">Google Certified</span>
    </div>
    <div class="links">
      <a class="link-btn link-gh" href="https://github.com/jenifervincya">⌥ GitHub</a>
      <a class="link-btn link-li" href="https://www.linkedin.com/in/jenifer-vincy-a-ab569b325">in LinkedIn</a>
      <a class="link-btn link-gm" href="mailto:jenifervincy@gmail.com">✉ Email</a>
    </div>
  </div>

  <div class="section-label">metrics</div>
  <div class="stats-grid">
    <div class="stat-card"><div class="stat-ico">🎓</div><span class="stat-val">8.79</span><div class="stat-lbl">CGPA</div></div>
    <div class="stat-card"><div class="stat-ico">💻</div><span class="stat-val">160+</span><div class="stat-lbl">LeetCode solved</div></div>
    <div class="stat-card"><div class="stat-ico">🍴</div><span class="stat-val">600+</span><div class="stat-lbl">CodeChef problems</div></div>
    <div class="stat-card"><div class="stat-ico">🏆</div><span class="stat-val">5+</span><div class="stat-lbl">Hackathons</div></div>
    <div class="stat-card"><div class="stat-ico">🤝</div><span class="stat-val">2yr</span><div class="stat-lbl">IEEE membership</div></div>
    <div class="stat-card"><div class="stat-ico">📦</div><span class="stat-val">4</span><div class="stat-lbl">Featured projects</div></div>
  </div>

  <div class="section-label">featured projects</div>
  <div class="projects">
    <div class="proj-card">
      <div class="proj-name">⚡ BoltOn.AI</div>
      <div class="proj-desc">Industrial IoT predictive maintenance platform with real-time anomaly detection and plug-and-play deployment.</div>
      <div class="proj-tags">
        <span class="tag">ESP32</span><span class="tag">Edge AI</span><span class="tag">FFT</span><span class="tag tag-t">One-Class SVM</span><span class="tag">IoT</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-name">🔋 EDGE-AI Smart Auditor</div>
      <div class="proj-desc">Decentralized harmonic analysis and NILM diagnostics for smart energy management and embedded analytics.</div>
      <div class="proj-tags">
        <span class="tag">STM32</span><span class="tag">NILM</span><span class="tag tag-t">Edge AI</span><span class="tag">IoT</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-name">🚑 ResQPath</div>
      <div class="proj-desc">Intelligent adaptive traffic signal system with ambulance detection, remote monitoring, and smart city integration.</div>
      <div class="proj-tags">
        <span class="tag">ESP32</span><span class="tag">RFID</span><span class="tag tag-t">Blynk IoT</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-name">🌍 Wander & Wonder</div>
      <div class="proj-desc">Responsive travel website with semantic HTML5 and clean UI — deployed via GitHub Pages.</div>
      <div class="proj-tags">
        <span class="tag">HTML5</span><span class="tag">CSS3</span><span class="tag tag-t">GitHub Pages</span>
      </div>
    </div>
  </div>

  <div class="section-label">tech stack</div>
  <div class="stack-section">
    <div class="stack-row">
      <div class="stack-lbl">Languages</div>
      <div class="pills"><span class="pill pill-hi">C</span><span class="pill pill-hi">C++</span><span class="pill pill-hi">Python</span><span class="pill pill-hi">Embedded C</span></div>
    </div>
    <div class="stack-row">
      <div class="stack-lbl">Platforms & Hardware</div>
      <div class="pills"><span class="pill">STM32</span><span class="pill">ESP32</span><span class="pill">Arduino</span><span class="pill">MPLAB X</span><span class="pill">PCB Design</span></div>
    </div>
    <div class="stack-row">
      <div class="stack-lbl">Protocols</div>
      <div class="pills"><span class="pill">UART</span><span class="pill">I2C</span><span class="pill">SPI</span><span class="pill">Bluetooth</span><span class="pill">RFID</span></div>
    </div>
    <div class="stack-row">
      <div class="stack-lbl">Tools & IoT Platforms</div>
      <div class="pills"><span class="pill">STM32CubeIDE</span><span class="pill">Autodesk EAGLE</span><span class="pill">TinkerCAD</span><span class="pill">ThingSpeak</span><span class="pill">Blynk</span><span class="pill">Git</span></div>
    </div>
    <div class="stack-row">
      <div class="stack-lbl">AI / Signal Processing</div>
      <div class="pills"><span class="pill">TinyML</span><span class="pill">FFT Analysis</span><span class="pill">Anomaly Detection</span><span class="pill">NILM</span></div>
    </div>
  </div>

  <div class="section-label">experience</div>
  <div style="margin-bottom:2.5rem">
    <div class="exp-item">
      <div class="exp-dot dot-amber">🔧</div>
      <div>
        <div class="exp-role">Industrial Training — Sunshiv Electronic Solutions</div>
        <div class="exp-org">Coimbatore · Dec 2025</div>
        <div class="exp-pts">PCB design & assembly · Autodesk EAGLE · Circuit design & troubleshooting · Product manufacturing exposure</div>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-dot dot-teal">⚡</div>
      <div>
        <div class="exp-role">Arduino Internship — Pantech Solutions</div>
        <div class="exp-org">Online · Dec 2025</div>
        <div class="exp-pts">Embedded application dev · Sensor interfacing · UART, I²C, Bluetooth, RFID · IoT with ThingSpeak</div>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-dot dot-blue">🚀</div>
      <div>
        <div class="exp-role">Embedded Systems Intern — iQuants Engineering Solutions</div>
        <div class="exp-org">Current</div>
        <div class="exp-pts">Automotive ECU development · Software Defined Vehicles (SDV) · Practical embedded engineering applications</div>
      </div>
    </div>
  </div>

  <div class="section-label">achievements</div>
  <div class="ach-grid">
    <div class="ach-item"><div class="ach-dot"></div>Smart India Hackathon 2025 — Selected (SIH25085)</div>
    <div class="ach-item"><div class="ach-dot"></div>TECHNOXIAN 9.0 World Robotics Championship</div>
    <div class="ach-item"><div class="ach-dot"></div>HackSmart 36-Hr Hackathon — Waste to Watts</div>
    <div class="ach-item"><div class="ach-dot"></div>TNWISE 2025 by TANCAM</div>
    <div class="ach-item"><div class="ach-dot"></div>TN-IMPACT 2026 by TANCAM</div>
    <div class="ach-item"><div class="ach-dot"></div>Google Prompting Essentials — Certified</div>
  </div>

  <div class="section-label">certifications</div>
  <div class="cert-cols">
    <div class="cert-group">
      <div class="cert-title">AI & Software</div>
      <div class="cert-item"><span class="cert-check">✓</span>Google Prompting Essentials</div>
      <div class="cert-item"><span class="cert-check">✓</span>AI Primer — Infosys Springboard</div>
      <div class="cert-item"><span class="cert-check">✓</span>Deep Learning & AI — CodeChef</div>
      <div class="cert-item"><span class="cert-check">✓</span>Python Foundation — Infosys</div>
    </div>
    <div class="cert-group">
      <div class="cert-title">Engineering & Dev</div>
      <div class="cert-item"><span class="cert-check">✓</span>IoT Boards Programming — POSTECH</div>
      <div class="cert-item"><span class="cert-check">✓</span>Git and GitHub — CodeChef</div>
      <div class="cert-item"><span class="cert-check">✓</span>C and C++ Programming</div>
      <div class="cert-item"><span class="cert-check">✓</span>Design Thinking — NPTEL</div>
    </div>
  </div>

  <div class="section-label">currently learning</div>
  <div class="learn-grid">
    <span class="learn-item">STM32 Peripheral Programming</span>
    <span class="learn-item">Industrial IoT Architectures</span>
    <span class="learn-item">Edge AI Deployment</span>
    <span class="learn-item">TinyML</span>
    <span class="learn-item">Embedded Linux</span>
    <span class="learn-item">German A1</span>
  </div>

  <div class="footer">
    <div class="footer-quote">// <span>Build things that matter.</span> Embed intelligence everywhere.</div>
    <div class="ieee">🤝 IEEE Student Member · 2024–Present · Active 2+ years</div>
  </div>

</div>
