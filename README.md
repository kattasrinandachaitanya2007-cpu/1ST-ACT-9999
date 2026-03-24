# 1ST-ACT-9999
THIS  IS FOR  ONLY START UPS, BY SNCK
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Nexara — Build What's Next</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet" />
<style>
  :root {
    --black: #080808;
    --white: #f5f3ee;
    --cream: #ede9e0;
    --accent: #c8f03c;
    --accent2: #3cffc8;
    --muted: #6b6860;
    --card-bg: #111110;
    --border: rgba(245,243,238,0.1);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--black);
    color: var(--white);
    font-family: 'DM Sans', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }
  h1,h2,h3,h4,h5 { font-family: 'Syne', sans-serif; line-height: 1.1; }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.25rem 4rem;
    border-bottom: 1px solid var(--border);
    background: rgba(8,8,8,0.85);
    backdrop-filter: blur(16px);
  }
  .nav-logo {
    font-family: 'Syne', sans-serif;
    font-size: 1.4rem; font-weight: 800;
    letter-spacing: -0.03em; color: var(--white);
    text-decoration: none;
  }
  .nav-logo span { color: var(--accent); }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a { color: var(--muted); text-decoration: none; font-size: 0.875rem; font-weight: 400; letter-spacing: 0.02em; transition: color 0.2s; }
  .nav-links a:hover { color: var(--white); }
  .nav-cta {
    background: var(--accent); color: var(--black);
    padding: 0.6rem 1.4rem; border-radius: 100px;
    font-family: 'Syne', sans-serif; font-weight: 700; font-size: 0.85rem;
    text-decoration: none; letter-spacing: 0.01em;
    transition: transform 0.2s, background 0.2s;
  }
  .nav-cta:hover { transform: scale(1.04); background: #d4f54a; }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex; flex-direction: column; justify-content: flex-end;
    padding: 0 4rem 5rem;
    position: relative; overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 80% 60% at 60% 40%, rgba(200,240,60,0.07) 0%, transparent 60%),
                radial-gradient(ellipse 50% 50% at 20% 80%, rgba(60,255,200,0.05) 0%, transparent 50%);
  }
  .hero-grid {
    position: absolute; inset: 0;
    background-image: linear-gradient(var(--border) 1px, transparent 1px),
                      linear-gradient(90deg, var(--border) 1px, transparent 1px);
    background-size: 80px 80px;
    mask-image: radial-gradient(ellipse 80% 70% at 50% 50%, black 30%, transparent 100%);
  }
  .hero-tag {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(200,240,60,0.1); border: 1px solid rgba(200,240,60,0.3);
    color: var(--accent); padding: 0.4rem 1rem; border-radius: 100px;
    font-size: 0.78rem; font-weight: 500; letter-spacing: 0.06em; text-transform: uppercase;
    margin-bottom: 2rem; width: fit-content;
    animation: fadeUp 0.8s ease both;
  }
  .hero-tag::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: var(--accent); }
  .hero h1 {
    font-size: clamp(3.5rem, 8vw, 7.5rem);
    font-weight: 800; letter-spacing: -0.04em;
    line-height: 0.95;
    max-width: 900px;
    animation: fadeUp 0.8s 0.1s ease both;
  }
  .hero h1 em { font-style: italic; font-weight: 400; color: var(--muted); }
  .hero-sub {
    margin-top: 2rem; max-width: 480px;
    color: var(--muted); font-size: 1.05rem; font-weight: 300; line-height: 1.7;
    animation: fadeUp 0.8s 0.2s ease both;
  }
  .hero-actions {
    display: flex; align-items: center; gap: 1.5rem; margin-top: 2.5rem;
    animation: fadeUp 0.8s 0.3s ease both;
  }
  .btn-primary {
    background: var(--accent); color: var(--black);
    padding: 0.9rem 2rem; border-radius: 100px;
    font-family: 'Syne', sans-serif; font-weight: 700; font-size: 0.9rem;
    text-decoration: none; letter-spacing: 0.01em;
    transition: transform 0.2s, box-shadow 0.2s;
    display: inline-flex; align-items: center; gap: 8px;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 12px 40px rgba(200,240,60,0.3); }
  .btn-primary svg { width: 16px; height: 16px; }
  .btn-ghost {
    color: var(--muted); font-size: 0.9rem; text-decoration: none;
    display: inline-flex; align-items: center; gap: 6px;
    transition: color 0.2s; border-bottom: 1px solid transparent;
    padding-bottom: 2px;
  }
  .btn-ghost:hover { color: var(--white); border-color: var(--white); }
  .hero-stats {
    position: absolute; right: 4rem; bottom: 5rem;
    display: flex; flex-direction: column; gap: 2rem;
    animation: fadeUp 0.8s 0.4s ease both;
  }
  .stat { text-align: right; }
  .stat-num { font-family: 'Syne', sans-serif; font-size: 2.2rem; font-weight: 800; color: var(--white); }
  .stat-label { font-size: 0.78rem; color: var(--muted); letter-spacing: 0.05em; text-transform: uppercase; }

  /* MARQUEE */
  .marquee-wrap {
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    padding: 1rem 0; overflow: hidden; background: var(--card-bg);
  }
  .marquee { display: flex; gap: 3rem; animation: marquee 20s linear infinite; white-space: nowrap; }
  .marquee-item { font-family: 'Syne', sans-serif; font-size: 0.8rem; font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase; color: var(--muted); display: flex; align-items: center; gap: 1rem; }
  .marquee-item::after { content: '?'; color: var(--accent); font-size: 0.7rem; }
  @keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

  /* SERVICES */
  .section { padding: 7rem 4rem; }
  .section-label {
    display: inline-flex; align-items: center; gap: 8px;
    font-size: 0.75rem; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--accent); margin-bottom: 1rem;
  }
  .section-label::before { content: ''; width: 24px; height: 1px; background: var(--accent); }
  .section-title { font-size: clamp(2.2rem, 4vw, 3.5rem); font-weight: 800; letter-spacing: -0.03em; max-width: 600px; }
  .section-title em { font-style: italic; color: var(--muted); font-weight: 400; }
  .services-grid {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 1px; background: var(--border);
    border: 1px solid var(--border);
    border-radius: 16px; overflow: hidden;
    margin-top: 4rem;
  }
  .service-card {
    background: var(--card-bg); padding: 2.5rem;
    position: relative; overflow: hidden;
    transition: background 0.3s;
    cursor: default;
  }
  .service-card:hover { background: #181817; }
  .service-card:hover .service-icon { background: rgba(200,240,60,0.15); color: var(--accent); }
  .service-num {
    font-family: 'Syne', sans-serif; font-size: 0.7rem; font-weight: 700;
    letter-spacing: 0.1em; color: var(--muted); margin-bottom: 1.5rem;
  }
  .service-icon {
    width: 48px; height: 48px; border-radius: 12px;
    background: rgba(245,243,238,0.06);
    display: flex; align-items: center; justify-content: center;
    font-size: 1.3rem; margin-bottom: 1.5rem;
    transition: background 0.3s, color 0.3s;
  }
  .service-card h3 { font-size: 1.25rem; font-weight: 700; margin-bottom: 0.75rem; }
  .service-card p { font-size: 0.875rem; color: var(--muted); line-height: 1.7; }
  .service-arrow {
    position: absolute; bottom: 2rem; right: 2rem;
    color: var(--muted); font-size: 1.2rem; opacity: 0;
    transition: opacity 0.2s, transform 0.2s;
  }
  .service-card:hover .service-arrow { opacity: 1; transform: translate(3px,-3px); }

  /* PROCESS */
  .process-section { background: var(--card-bg); }
  .process-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 6rem; align-items: center; margin-top: 4rem;
  }
  .process-steps { display: flex; flex-direction: column; gap: 0; }
  .process-step {
    display: flex; gap: 1.5rem; padding: 2rem 0;
    border-bottom: 1px solid var(--border);
    position: relative;
  }
  .step-num {
    font-family: 'Syne', sans-serif; font-size: 0.7rem; font-weight: 700;
    letter-spacing: 0.1em; color: var(--accent); min-width: 36px; padding-top: 4px;
  }
  .step-content h4 { font-size: 1rem; font-weight: 700; margin-bottom: 0.4rem; }
  .step-content p { font-size: 0.85rem; color: var(--muted); line-height: 1.6; }
  .process-visual {
    aspect-ratio: 1; background: var(--black);
    border-radius: 24px; position: relative; overflow: hidden;
    border: 1px solid var(--border);
    display: flex; align-items: center; justify-content: center;
  }
  .pv-ring {
    position: absolute; border-radius: 50%;
    border: 1px solid rgba(200,240,60,0.15);
    animation: pulse 3s ease-in-out infinite;
  }
  .pv-ring:nth-child(1) { width: 160px; height: 160px; animation-delay: 0s; }
  .pv-ring:nth-child(2) { width: 260px; height: 260px; animation-delay: 0.5s; }
  .pv-ring:nth-child(3) { width: 360px; height: 360px; animation-delay: 1s; }
  .pv-center {
    width: 80px; height: 80px; border-radius: 50%;
    background: rgba(200,240,60,0.12);
    border: 1px solid rgba(200,240,60,0.4);
    display: flex; align-items: center; justify-content: center;
    font-size: 1.8rem; position: relative; z-index: 2;
  }
  @keyframes pulse { 0%,100% { opacity: 0.4; transform: scale(1); } 50% { opacity: 0.8; transform: scale(1.03); } }

  /* PRICING */
  .pricing-grid {
    display: grid; grid-template-columns: repeat(3,1fr);
    gap: 1.5rem; margin-top: 4rem;
  }
  .price-card {
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 20px; padding: 2.5rem; position: relative;
    transition: transform 0.3s, border-color 0.3s;
  }
  .price-card:hover { transform: translateY(-4px); }
  .price-card.featured {
    border-color: var(--accent);
    background: linear-gradient(160deg, rgba(200,240,60,0.06) 0%, var(--card-bg) 60%);
  }
  .price-card.featured::before {
    content: 'Most Popular';
    position: absolute; top: -12px; left: 50%; transform: translateX(-50%);
    background: var(--accent); color: var(--black);
    font-family: 'Syne', sans-serif; font-size: 0.7rem; font-weight: 700;
    letter-spacing: 0.08em; text-transform: uppercase;
    padding: 4px 14px; border-radius: 100px;
  }
  .price-tier { font-size: 0.75rem; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase; color: var(--muted); margin-bottom: 1rem; }
  .price-num { font-family: 'Syne', sans-serif; font-size: 3rem; font-weight: 800; }
  .price-num sup { font-size: 1.2rem; vertical-align: super; margin-right: 2px; }
  .price-num span { font-size: 1rem; color: var(--muted); font-weight: 400; }
  .price-desc { font-size: 0.85rem; color: var(--muted); margin: 0.75rem 0 1.5rem; line-height: 1.6; }
  .price-features { list-style: none; display: flex; flex-direction: column; gap: 0.7rem; margin-bottom: 2rem; }
  .price-features li { font-size: 0.85rem; color: var(--muted); display: flex; gap: 10px; align-items: flex-start; }
  .price-features li::before { content: '?'; color: var(--accent); font-weight: 700; flex-shrink: 0; }
  .price-btn {
    display: block; text-align: center; padding: 0.8rem;
    border-radius: 100px; font-family: 'Syne', sans-serif; font-weight: 700; font-size: 0.85rem;
    text-decoration: none; transition: all 0.2s; letter-spacing: 0.01em;
  }
  .price-btn-outline { border: 1px solid var(--border); color: var(--white); }
  .price-btn-outline:hover { border-color: var(--white); }
  .price-btn-solid { background: var(--accent); color: var(--black); }
  .price-btn-solid:hover { background: #d4f54a; transform: translateY(-1px); }

  /* TESTIMONIALS */
  .testimonials-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; margin-top: 4rem; }
  .testi-card {
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 20px; padding: 2rem;
  }
  .testi-stars { color: var(--accent); font-size: 0.85rem; letter-spacing: 2px; margin-bottom: 1rem; }
  .testi-text { font-size: 0.95rem; line-height: 1.75; color: var(--white); margin-bottom: 1.5rem; font-style: italic; font-weight: 300; }
  .testi-author { display: flex; align-items: center; gap: 12px; }
  .testi-avatar {
    width: 40px; height: 40px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Syne', sans-serif; font-weight: 700; font-size: 0.85rem;
    background: rgba(200,240,60,0.12); color: var(--accent);
    border: 1px solid rgba(200,240,60,0.25);
  }
  .testi-name { font-size: 0.85rem; font-weight: 500; }
  .testi-role { font-size: 0.75rem; color: var(--muted); }

  /* CTA */
  .cta-section {
    margin: 0 4rem 7rem;
    background: linear-gradient(135deg, rgba(200,240,60,0.08) 0%, transparent 60%);
    border: 1px solid rgba(200,240,60,0.2);
    border-radius: 28px; padding: 5rem;
    text-align: center; position: relative; overflow: hidden;
  }
  .cta-section::before {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(circle at 50% 0%, rgba(200,240,60,0.12), transparent 60%);
    pointer-events: none;
  }
  .cta-section h2 { font-size: clamp(2.5rem, 5vw, 4rem); font-weight: 800; letter-spacing: -0.03em; margin-bottom: 1rem; }
  .cta-section p { color: var(--muted); font-size: 1.05rem; max-width: 480px; margin: 0 auto 2.5rem; line-height: 1.7; }
  .cta-actions { display: flex; gap: 1rem; justify-content: center; align-items: center; flex-wrap: wrap; }

  /* FOOTER */
  footer {
    border-top: 1px solid var(--border);
    padding: 3rem 4rem;
    display: flex; justify-content: space-between; align-items: center;
    flex-wrap: wrap; gap: 1rem;
  }
  .footer-logo { font-family: 'Syne', sans-serif; font-size: 1.1rem; font-weight: 800; color: var(--white); }
  .footer-logo span { color: var(--accent); }
  .footer-links { display: flex; gap: 2rem; }
  .footer-links a { color: var(--muted); text-decoration: none; font-size: 0.82rem; transition: color 0.2s; }
  .footer-links a:hover { color: var(--white); }
  .footer-copy { color: var(--muted); font-size: 0.78rem; }

  @keyframes fadeUp { from { opacity: 0; transform: translateY(24px); } to { opacity: 1; transform: translateY(0); } }

  /* MOBILE */
  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { padding: 0 1.5rem 4rem; }
    .hero-stats { display: none; }
    .section { padding: 5rem 1.5rem; }
    .services-grid { grid-template-columns: 1fr; }
    .process-grid { grid-template-columns: 1fr; gap: 3rem; }
    .pricing-grid { grid-template-columns: 1fr; }
    .testimonials-grid { grid-template-columns: 1fr; }
    .cta-section { margin: 0 1.5rem 5rem; padding: 3rem 1.5rem; }
    footer { padding: 2rem 1.5rem; flex-direction: column; align-items: flex-start; gap: 1.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Nex<span>ara</span></a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#pricing">Pricing</a></li>
    <li><a href="#testimonials">Results</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Get Started</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-tag">Startup Growth Partners</div>
  <h1>Build your<br><em>next</em> big<br>thing.</h1>
  <p class="hero-sub">We help ambitious startups scale faster — with strategy, design, and technology that moves at the speed of your vision.</p>
  <div class="hero-actions">
    <a href="#pricing" class="btn-primary">
      See Our Services
      <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 8h10M9 4l4 4-4 4"/></svg>
    </a>
    <a href="#process" class="btn-ghost">How it works ?</a>
  </div>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num">200+</div><div class="stat-label">Startups Scaled</div></div>
    <div class="stat"><div class="stat-num">$40M+</div><div class="stat-label">Revenue Generated</div></div>
    <div class="stat"><div class="stat-num">98%</div><div class="stat-label">Client Retention</div></div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee">
    <span class="marquee-item">Growth Strategy</span>
    <span class="marquee-item">Product Design</span>
    <span class="marquee-item">Go-to-Market</span>
    <span class="marquee-item">Brand Identity</span>
    <span class="marquee-item">Tech Development</span>
    <span class="marquee-item">Investor Decks</span>
    <span class="marquee-item">Scaling Systems</span>
    <span class="marquee-item">Revenue Ops</span>
    <span class="marquee-item">Growth Strategy</span>
    <span class="marquee-item">Product Design</span>
    <span class="marquee-item">Go-to-Market</span>
    <span class="marquee-item">Brand Identity</span>
    <span class="marquee-item">Tech Development</span>
    <span class="marquee-item">Investor Decks</span>
    <span class="marquee-item">Scaling Systems</span>
    <span class="marquee-item">Revenue Ops</span>
  </div>
</div>

<!-- SERVICES -->
<section class="section" id="services">
  <div class="section-label">What We Do</div>
  <h2 class="section-title">Services built for <em>velocity.</em></h2>
  <div class="services-grid">
    <div class="service-card">
      <div class="service-num">01</div>
      <div class="service-icon">??</div>
      <h3>Growth Strategy</h3>
      <p>Data-driven growth frameworks tailored to your market. From acquisition funnels to retention loops — we build the engine.</p>
      <div class="service-arrow">?</div>
    </div>
    <div class="service-card">
      <div class="service-num">02</div>
      <div class="service-icon">?</div>
      <h3>Brand & Design</h3>
      <p>Distinctive identities that command attention. Visual systems, messaging, and positioning that sets you apart from day one.</p>
      <div class="service-arrow">?</div>
    </div>
    <div class="service-card">
      <div class="service-num">03</div>
      <div class="service-icon">?</div>
      <h3>Product Development</h3>
      <p>End-to-end product builds — from wireframes to launch-ready software. Fast iterations, clean code, scalable architecture.</p>
      <div class="service-arrow">?</div>
    </div>
    <div class="service-card">
      <div class="service-num">04</div>
      <div class="service-icon">??</div>
      <h3>Go-to-Market</h3>
      <p>Launch playbooks that drive real traction. Competitive positioning, channel strategy, and launch campaigns that convert.</p>
      <div class="service-arrow">?</div>
    </div>
    <div class="service-card">
      <div class="service-num">05</div>
      <div class="service-icon">??</div>
      <h3>Investor Readiness</h3>
      <p>Pitch decks, financial models, and narrative strategy to help you close your next round with confidence.</p>
      <div class="service-arrow">?</div>
    </div>
    <div class="service-card">
      <div class="service-num">06</div>
      <div class="service-icon">??</div>
      <h3>Revenue Operations</h3>
      <p>Sales infrastructure, CRM systems, and pipeline automation to turn leads into loyal customers at scale.</p>
      <div class="service-arrow">?</div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="section process-section" id="process">
  <div class="section-label">How It Works</div>
  <h2 class="section-title">From idea to <em>impact</em> — fast.</h2>
  <div class="process-grid">
    <div class="process-steps">
      <div class="process-step">
        <div class="step-num">01</div>
        <div class="step-content">
          <h4>Discovery & Audit</h4>
          <p>We deep-dive into your business, market, and goals to identify your highest-leverage opportunities.</p>
        </div>
      </div>
      <div class="process-step">
        <div class="step-num">02</div>
        <div class="step-content">
          <h4>Strategy Blueprint</h4>
          <p>A custom roadmap with clear milestones, priorities, and success metrics designed for your stage.</p>
        </div>
      </div>
      <div class="process-step">
        <div class="step-num">03</div>
        <div class="step-content">
          <h4>Execution Sprint</h4>
          <p>Our team moves fast — building, testing, and iterating in tight cycles to maintain momentum.</p>
        </div>
      </div>
      <div class="process-step">
        <div class="step-num">04</div>
        <div class="step-content">
          <h4>Scale & Optimize</h4>
          <p>Continuous refinement and growth — we stay in your corner as you scale to the next level.</p>
        </div>
      </div>
    </div>
    <div class="process-visual">
      <div class="pv-ring"></div>
      <div class="pv-ring"></div>
      <div class="pv-ring"></div>
      <div class="pv-center">?</div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section class="section" id="pricing">
  <div class="section-label">Pricing</div>
  <h2 class="section-title">Transparent plans, <em>real results.</em></h2>
  <div class="pricing-grid">
    <div class="price-card">
      <div class="price-tier">Starter</div>
      <div class="price-num"><sup>$</sup>2,499<span>/mo</span></div>
      <p class="price-desc">Perfect for early-stage startups ready to build their foundation.</p>
      <ul class="price-features">
        <li>Growth strategy audit</li>
        <li>Brand identity kit</li>
        <li>Go-to-market playbook</li>
        <li>2 strategy calls/month</li>
        <li>Slack support channel</li>
      </ul>
      <a href="#contact" class="price-btn price-btn-outline">Get Started</a>
    </div>
    <div class="price-card featured">
      <div class="price-tier">Growth</div>
      <div class="price-num"><sup>$</sup>5,999<span>/mo</span></div>
      <p class="price-desc">For startups accelerating toward product-market fit and first revenue.</p>
      <ul class="price-features">
        <li>Everything in Starter</li>
        <li>Full product development</li>
        <li>Investor deck creation</li>
        <li>Revenue ops setup</li>
        <li>Weekly performance reviews</li>
        <li>Dedicated growth lead</li>
      </ul>
      <a href="#contact" class="price-btn price-btn-solid">Get Started</a>
    </div>
    <div class="price-card">
      <div class="price-tier">Scale</div>
      <div class="price-num"><sup>$</sup>12,999<span>/mo</span></div>
      <p class="price-desc">For Series A+ startups scaling operations and accelerating growth.</p>
      <ul class="price-features">
        <li>Everything in Growth</li>
        <li>Embedded team of experts</li>
        <li>Custom tech architecture</li>
        <li>Fundraising support</li>
        <li>Executive advisory access</li>
        <li>Priority 24/7 support</li>
      </ul>
      <a href="#contact" class="price-btn price-btn-outline">Get Started</a>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="section" id="testimonials" style="background: var(--card-bg);">
  <div class="section-label">Client Results</div>
  <h2 class="section-title">Words from <em>founders</em> we've built with.</h2>
  <div class="testimonials-grid">
    <div class="testi-card">
      <div class="testi-stars">?????</div>
      <p class="testi-text">"Nexara helped us go from zero to $1.2M ARR in under 8 months. Their growth strategy was unlike anything we'd seen — data-driven, fast, and completely tailored to our market."</p>
      <div class="testi-author">
        <div class="testi-avatar">AK</div>
        <div><div class="testi-name">Anika Kapoor</div><div class="testi-role">CEO, Flowlabs</div></div>
      </div>
    </div>
    <div class="testi-card">
      <div class="testi-stars">?????</div>
      <p class="testi-text">"We closed our seed round 3 weeks after working with Nexara on our pitch and investor narrative. The clarity they brought to our story was transformative."</p>
      <div class="testi-author">
        <div class="testi-avatar">MR</div>
        <div><div class="testi-name">Marcus Reid</div><div class="testi-role">Founder, Arclight AI</div></div>
      </div>
    </div>
    <div class="testi-card">
      <div class="testi-stars">?????</div>
      <p class="testi-text">"The product we built with Nexara launched on time, under budget, and with a 4.9-star rating from day one. Their team genuinely cares about outcomes, not just deliverables."</p>
      <div class="testi-author">
        <div class="testi-avatar">SL</div>
        <div><div class="testi-name">Sophia Lin</div><div class="testi-role">CTO, Verda Health</div></div>
      </div>
    </div>
    <div class="testi-card">
      <div class="testi-stars">?????</div>
      <p class="testi-text">"Our brand was forgettable before Nexara. Now we're recognized as a category leader. The rebranding and positioning work paid for itself within the first quarter."</p>
      <div class="testi-author">
        <div class="testi-avatar">JO</div>
        <div><div class="testi-name">James Osei</div><div class="testi-role">Co-founder, Stackr</div></div>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta-section" id="contact">
  <h2>Ready to build <br>something remarkable?</h2>
  <p>Let's talk about your startup and map out the fastest path to traction, funding, or scale.</p>
  <div class="cta-actions">
    <a href="mailto:hello@nexara.co" class="btn-primary">
      Book a Free Call
      <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2" style="width:16px;height:16px;"><path d="M3 8h10M9 4l4 4-4 4"/></svg>
    </a>
    <a href="#services" class="btn-ghost" style="color: var(--muted);">Explore services ?</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Nex<span>ara</span></div>
  <nav class="footer-links">
    <a href="#services">Services</a>
    <a href="#process">Process</a>
    <a href="#pricing">Pricing</a>
    <a href="#contact">Contact</a>
  </nav>
  <div class="footer-copy">© 2026 Nexara. All rights reserved.</div>
</footer>

<script>
  // Smooth scroll offset for fixed nav
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      const target = document.querySelector(a.getAttribute('href'));
      if (target) {
        e.preventDefault();
        window.scrollTo({ top: target.offsetTop - 80, behavior: 'smooth' });
      }
    });
  });

  // Scroll reveal
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.service-card, .price-card, .testi-card, .process-step').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(20px)';
    el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
    observer.observe(el);
  });
</script>
</body>
</html>
