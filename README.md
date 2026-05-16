# RIDGELINE
/Users/lukasolin/Desktop/Claude-CoWork-Agancy/Kira-Web Design-Agancy/_portfolio/ridgeline-roofing/index.html
[index.html](https://github.com/user-attachments/files/27860602/index.html)<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ridgeline Roofing &amp; Construction | Manchester</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <style>
    /* ─── VARIABLES ─────────────────────────────────────────── */
    :root {
      --bg:        #0C1017;
      --bg2:       #141A24;
      --bg3:       #1B2133;
      --bg4:       #212840;
      --text:      #F0F2F5;
      --text2:     #8B95A8;
      --text3:     #5A6478;
      --accent:    #D4611A;
      --accent-h:  #E8721D;
      --accent-d:  #B85516;
      --border:    #252F45;
      --white:     #FFFFFF;
      --nav-h:     72px;
      --shadow:    0 4px 24px rgba(0,0,0,.45);
      --shadow-lg: 0 12px 48px rgba(0,0,0,.6);
      --radius:    8px;
      --radius-lg: 16px;
      --transition: 0.28s ease;
    }

    /* ─── RESET ─────────────────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; font-size: 16px; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.65;
      overflow-x: hidden;
    }
    a { color: inherit; text-decoration: none; }
    img { display: block; max-width: 100%; }
    ul { list-style: none; }
    button { cursor: pointer; border: none; background: none; font: inherit; }
    svg { display: block; }

    /* ─── TYPOGRAPHY ─────────────────────────────────────────── */
    h1, h2, h3, h4 {
      font-family: 'Barlow Condensed', sans-serif;
      letter-spacing: 0.02em;
      line-height: 1.1;
      font-weight: 700;
    }
    h1 { font-size: clamp(2.6rem, 6vw, 5rem); }
    h2 { font-size: clamp(2rem, 4vw, 3rem); font-weight: 800; }
    h3 { font-size: clamp(1.4rem, 2.5vw, 1.9rem); }
    h4 { font-size: 1.15rem; font-weight: 600; }
    p { color: var(--text2); font-weight: 400; }
    .label {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 0.8rem;
      font-weight: 600;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--accent);
    }

    /* ─── PAGE SYSTEM ─────────────────────────────────────────── */
    .page { display: none; }
    .page.active { display: block; }

    /* ─── SCROLLBAR ─────────────────────────────────────────── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--accent); border-radius: 3px; }

    /* ─── NAVIGATION ─────────────────────────────────────────── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      height: var(--nav-h);
      background: rgba(12,16,23,0.88);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 5%;
      z-index: 999;
      transition: background var(--transition);
    }
    nav.scrolled { background: rgba(12,16,23,0.98); }

    .nav-logo {
      display: flex;
      flex-direction: column;
      line-height: 1;
      cursor: pointer;
    }
    .nav-logo .wordmark {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.5rem;
      font-weight: 800;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--white);
    }
    .nav-logo .wordmark span { color: var(--accent); }
    .nav-logo .sub {
      font-size: 0.62rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--text2);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 2rem;
    }
    .nav-links a {
      font-size: 0.88rem;
      font-weight: 500;
      letter-spacing: 0.04em;
      color: var(--text2);
      transition: color var(--transition);
      cursor: pointer;
    }
    .nav-links a:hover,
    .nav-links a.active { color: var(--white); }
    .nav-links a.active::after {
      content: '';
      display: block;
      height: 2px;
      background: var(--accent);
      margin-top: 2px;
      border-radius: 1px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.65rem 1.4rem;
      border-radius: var(--radius);
      font-weight: 600;
      font-size: 0.88rem;
      letter-spacing: 0.04em;
      transition: all var(--transition);
      cursor: pointer;
    }
    .btn-primary {
      background: var(--accent);
      color: var(--white);
    }
    .btn-primary:hover {
      background: var(--accent-h);
      transform: translateY(-1px);
      box-shadow: 0 6px 20px rgba(212,97,26,.35);
    }
    .btn-outline {
      border: 1.5px solid rgba(255,255,255,0.25);
      color: var(--white);
    }
    .btn-outline:hover {
      border-color: var(--white);
      background: rgba(255,255,255,0.06);
    }
    .btn-lg { padding: 0.85rem 2rem; font-size: 1rem; }

    /* Hamburger */
    .hamburger {
      display: none;
      flex-direction: column;
      gap: 5px;
      padding: 6px;
      cursor: pointer;
    }
    .hamburger span {
      display: block;
      width: 24px;
      height: 2px;
      background: var(--text);
      border-radius: 2px;
      transition: all var(--transition);
    }
    .hamburger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
    .hamburger.open span:nth-child(2) { opacity: 0; }
    .hamburger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

    /* Mobile menu */
    .mobile-menu {
      display: none;
      position: fixed;
      top: var(--nav-h);
      left: 0; right: 0;
      background: var(--bg2);
      border-bottom: 1px solid var(--border);
      padding: 1.5rem 5%;
      flex-direction: column;
      gap: 1.25rem;
      z-index: 998;
    }
    .mobile-menu.open { display: flex; }
    .mobile-menu a {
      font-size: 1.1rem;
      font-weight: 500;
      color: var(--text2);
      transition: color var(--transition);
      cursor: pointer;
    }
    .mobile-menu a:hover { color: var(--white); }

    /* ─── SECTIONS & LAYOUT ──────────────────────────────────── */
    section { padding: 6rem 5%; }
    .container { max-width: 1200px; margin: 0 auto; }
    .section-head { text-align: center; margin-bottom: 4rem; }
    .section-head .label { margin-bottom: 0.75rem; }
    .section-head p { max-width: 560px; margin: 1rem auto 0; }

    /* ─── ICONS ──────────────────────────────────────────────── */
    .icon-wrap {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }
    .icon-wrap svg {
      stroke: var(--accent);
      fill: none;
      stroke-width: 1.5;
      stroke-linecap: round;
      stroke-linejoin: round;
    }

    /* ─── HOME: HERO ─────────────────────────────────────────── */
    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: var(--nav-h) 5% 0;
      overflow: hidden;
    }
    .hero-bg {
      position: absolute;
      inset: 0;
      background-image: url('https://images.unsplash.com/photo-1558618666-fcd25c85cd64?auto=format&fit=crop&w=1800&q=80');
      background-size: cover;
      background-position: center 40%;
      filter: brightness(0.3);
    }
    .hero-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(120deg, rgba(12,16,23,0.92) 50%, rgba(212,97,26,0.06) 100%);
    }
    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 760px;
    }
    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      background: rgba(212,97,26,0.12);
      border: 1px solid rgba(212,97,26,0.3);
      border-radius: 100px;
      padding: 0.35rem 1rem;
      font-size: 0.8rem;
      font-weight: 500;
      letter-spacing: 0.06em;
      color: var(--accent);
      margin-bottom: 1.75rem;
    }
    .hero-badge-dot {
      width: 6px;
      height: 6px;
      background: var(--accent);
      border-radius: 50%;
      flex-shrink: 0;
    }
    .hero h1 {
      margin-bottom: 1.25rem;
      text-transform: uppercase;
    }
    .hero h1 span { color: var(--accent); }
    .hero p {
      font-size: 1.1rem;
      color: var(--text2);
      max-width: 560px;
      margin-bottom: 2.5rem;
      font-weight: 300;
      line-height: 1.75;
    }
    .hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }

    /* Scroll indicator */
    .scroll-hint {
      position: absolute;
      bottom: 2.5rem;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.72rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--text3);
      z-index: 2;
      animation: bounce 2s ease-in-out infinite;
    }
    .scroll-hint::after {
      content: '';
      display: block;
      width: 1.5px;
      height: 36px;
      background: linear-gradient(to bottom, var(--accent), transparent);
    }
    @keyframes bounce {
      0%, 100% { transform: translateX(-50%) translateY(0); }
      50% { transform: translateX(-50%) translateY(6px); }
    }

    /* ─── HOME: STATS BAR ────────────────────────────────────── */
    .stats-bar {
      padding: 0 5%;
      background: var(--bg2);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }
    .stats-grid {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
    }
    .stat-item {
      padding: 2.5rem 2rem;
      text-align: center;
      border-right: 1px solid var(--border);
    }
    .stat-item:last-child { border-right: none; }
    .stat-num {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 3rem;
      font-weight: 800;
      color: var(--accent);
      line-height: 1;
      margin-bottom: 0.4rem;
    }
    .stat-label {
      font-size: 0.82rem;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--text2);
      font-weight: 500;
    }

    /* ─── HOME: SERVICES OVERVIEW ────────────────────────────── */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.5px;
      background: var(--border);
      border: 1.5px solid var(--border);
      border-radius: var(--radius-lg);
      overflow: hidden;
    }
    .service-card {
      background: var(--bg2);
      padding: 2.25rem 2rem;
      transition: background var(--transition);
      cursor: pointer;
    }
    .service-card:hover { background: var(--bg3); }
    .service-icon {
      width: 48px;
      height: 48px;
      background: rgba(212,97,26,0.1);
      border: 1px solid rgba(212,97,26,0.2);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1.25rem;
    }
    .service-icon svg {
      width: 22px;
      height: 22px;
      stroke: var(--accent);
      fill: none;
      stroke-width: 1.5;
      stroke-linecap: round;
      stroke-linejoin: round;
    }
    .service-card h4 {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.2rem;
      font-weight: 700;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      margin-bottom: 0.5rem;
      color: var(--white);
    }
    .service-card p { font-size: 0.88rem; line-height: 1.6; }

    /* ─── HOME: WHY RIDGELINE ────────────────────────────────── */
    .why-inner {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem;
      align-items: center;
      max-width: 1200px;
      margin: 0 auto;
    }
    .why-img {
      position: relative;
      border-radius: var(--radius-lg);
      overflow: hidden;
      aspect-ratio: 4/3;
    }
    .why-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .why-img::after {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: var(--radius-lg);
      border: 1.5px solid rgba(212,97,26,0.2);
      pointer-events: none;
    }
    .why-badge {
      position: absolute;
      bottom: 1.5rem;
      left: 1.5rem;
      background: var(--accent);
      color: var(--white);
      border-radius: var(--radius);
      padding: 1rem 1.25rem;
      font-family: 'Barlow Condensed', sans-serif;
    }
    .why-badge .num { font-size: 2.2rem; font-weight: 800; line-height: 1; }
    .why-badge .txt { font-size: 0.78rem; letter-spacing: 0.06em; text-transform: uppercase; }
    .why-points { display: flex; flex-direction: column; gap: 1.5rem; margin-top: 2rem; }
    .why-point {
      display: flex;
      gap: 1.25rem;
      align-items: flex-start;
    }
    .why-point-icon {
      flex-shrink: 0;
      width: 40px;
      height: 40px;
      background: rgba(212,97,26,0.1);
      border: 1px solid rgba(212,97,26,0.2);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 2px;
    }
    .why-point-icon svg {
      width: 18px;
      height: 18px;
      stroke: var(--accent);
      fill: none;
      stroke-width: 1.5;
      stroke-linecap: round;
      stroke-linejoin: round;
    }
    .why-point-text h4 {
      font-family: 'Inter', sans-serif;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--white);
      margin-bottom: 0.2rem;
    }
    .why-point-text p { font-size: 0.85rem; line-height: 1.6; }

    /* ─── HOME: TESTIMONIALS ─────────────────────────────────── */
    .testimonials-section { background: var(--bg2); }
    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.5rem;
      max-width: 1200px;
      margin: 0 auto;
    }
    .testimonial-card {
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 2rem;
      position: relative;
    }
    .testimonial-card::before {
      content: '"';
      position: absolute;
      top: 1rem;
      right: 1.5rem;
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 5rem;
      color: var(--accent);
      opacity: 0.12;
      line-height: 1;
    }
    .stars {
      display: flex;
      gap: 3px;
      margin-bottom: 1rem;
    }
    .stars svg {
      width: 15px;
      height: 15px;
      fill: var(--accent);
      stroke: none;
    }
    .testimonial-card p { font-size: 0.9rem; line-height: 1.7; font-style: italic; margin-bottom: 1.5rem; }
    .t-author { display: flex; align-items: center; gap: 0.75rem; }
    .t-avatar {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: var(--accent);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Barlow Condensed', sans-serif;
      font-weight: 700;
      font-size: 1rem;
      color: var(--white);
      flex-shrink: 0;
    }
    .t-name { font-weight: 600; font-size: 0.88rem; color: var(--white); }
    .t-loc { font-size: 0.78rem; color: var(--text3); }

    /* ─── CTA BANNER ─────────────────────────────────────────── */
    .cta-banner {
      background: linear-gradient(120deg, var(--accent-d) 0%, var(--accent) 100%);
      padding: 5rem 5%;
      text-align: center;
    }
    .cta-banner h2 { color: var(--white); margin-bottom: 1rem; }
    .cta-banner p { color: rgba(255,255,255,0.8); margin-bottom: 2rem; max-width: 480px; margin-left: auto; margin-right: auto; }
    .cta-banner .btn-white { background: var(--white); color: var(--accent); }
    .cta-banner .btn-white:hover { background: var(--bg); color: var(--white); box-shadow: none; }

    /* ─── PAGE HERO ──────────────────────────────────────────── */
    .page-hero {
      padding: calc(var(--nav-h) + 4rem) 5% 4rem;
      background: var(--bg2);
      border-bottom: 1px solid var(--border);
      text-align: center;
    }
    .page-hero .label { margin-bottom: 0.75rem; }
    .page-hero h1 { text-transform: uppercase; margin-bottom: 1rem; }
    .page-hero p { max-width: 600px; margin: 0 auto; font-size: 1.05rem; }

    /* ─── SERVICES PAGE ─────────────────────────────────────── */
    .services-full { display: flex; flex-direction: column; }
    .service-full-item {
      display: grid;
      grid-template-columns: 1fr 1fr;
      border-bottom: 1px solid var(--border);
    }
    .service-full-item.reverse { direction: rtl; }
    .service-full-item.reverse > * { direction: ltr; }
    .service-full-img {
      aspect-ratio: 16/10;
      overflow: hidden;
      background: var(--bg3);
    }
    .service-full-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    .service-full-item:hover .service-full-img img { transform: scale(1.03); }
    .service-full-body {
      padding: 3.5rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      background: var(--bg2);
    }
    .service-full-body .label { margin-bottom: 0.75rem; }
    .service-full-body h3 { text-transform: uppercase; margin-bottom: 1rem; }
    .service-full-body > p { margin-bottom: 1.5rem; line-height: 1.8; }
    .service-list { display: flex; flex-direction: column; gap: 0.6rem; margin-bottom: 2rem; }
    .service-list li {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      font-size: 0.88rem;
      color: var(--text2);
    }
    .service-list li svg {
      width: 14px;
      height: 14px;
      stroke: var(--accent);
      fill: none;
      stroke-width: 2.5;
      stroke-linecap: round;
      stroke-linejoin: round;
      flex-shrink: 0;
    }

    /* ─── ABOUT PAGE ─────────────────────────────────────────── */
    .about-story {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem;
      align-items: center;
      max-width: 1200px;
      margin: 0 auto;
    }
    .about-story-img {
      border-radius: var(--radius-lg);
      overflow: hidden;
      aspect-ratio: 3/4;
    }
    .about-story-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .about-story-text .label { margin-bottom: 0.75rem; }
    .about-story-text h2 { text-transform: uppercase; margin-bottom: 1.5rem; }
    .about-story-text p { margin-bottom: 1.25rem; line-height: 1.8; }

    .values-section { background: var(--bg2); }
    .values-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1.5rem;
      max-width: 1200px;
      margin: 0 auto;
    }
    .value-card {
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 2rem 1.5rem;
      text-align: center;
      transition: border-color var(--transition);
    }
    .value-card:hover { border-color: var(--accent); }
    .value-icon {
      width: 52px;
      height: 52px;
      background: rgba(212,97,26,0.1);
      border: 1px solid rgba(212,97,26,0.2);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 1rem;
    }
    .value-icon svg {
      width: 22px;
      height: 22px;
      stroke: var(--accent);
      fill: none;
      stroke-width: 1.5;
      stroke-linecap: round;
      stroke-linejoin: round;
    }
    .value-card h4 {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.1rem;
      font-weight: 700;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      color: var(--white);
      margin-bottom: 0.6rem;
    }
    .value-card p { font-size: 0.84rem; }

    .accreditations {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1.5rem;
    }
    .accred-card {
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }
    .accred-tag {
      display: inline-block;
      background: rgba(212,97,26,0.1);
      border: 1px solid rgba(212,97,26,0.2);
      border-radius: 4px;
      padding: 0.2rem 0.6rem;
      font-size: 0.72rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--accent);
      font-weight: 600;
      width: fit-content;
    }
    .accred-card h4 {
      font-family: 'Inter', sans-serif;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--white);
    }
    .accred-card p { font-size: 0.82rem; }

    /* ─── GALLERY PAGE ─────────────────────────────────────── */
    .gallery-filter {
      display: flex;
      gap: 0.75rem;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 3rem;
    }
    .filter-btn {
      padding: 0.5rem 1.25rem;
      border-radius: 100px;
      border: 1.5px solid var(--border);
      font-size: 0.84rem;
      font-weight: 500;
      color: var(--text2);
      transition: all var(--transition);
      cursor: pointer;
      background: transparent;
    }
    .filter-btn:hover { border-color: var(--accent); color: var(--accent); }
    .filter-btn.active { background: var(--accent); border-color: var(--accent); color: var(--white); }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.25rem;
      max-width: 1200px;
      margin: 0 auto;
    }
    .gallery-item {
      position: relative;
      border-radius: var(--radius-lg);
      overflow: hidden;
      aspect-ratio: 4/3;
      cursor: pointer;
      background: var(--bg3);
    }
    .gallery-item.wide { grid-column: span 2; aspect-ratio: 16/9; }
    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }
    .gallery-item:hover img { transform: scale(1.05); }
    .gallery-overlay {
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(12,16,23,0.85) 0%, transparent 50%);
      opacity: 0;
      transition: opacity var(--transition);
      display: flex;
      align-items: flex-end;
      padding: 1.5rem;
    }
    .gallery-item:hover .gallery-overlay { opacity: 1; }
    .gallery-overlay-text h4 {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.1rem;
      font-weight: 700;
      text-transform: uppercase;
      color: var(--white);
      margin-bottom: 0.25rem;
    }
    .gallery-overlay-text span {
      font-size: 0.78rem;
      color: var(--accent);
      letter-spacing: 0.08em;
      text-transform: uppercase;
      font-weight: 500;
    }

    /* ─── CONTACT PAGE ─────────────────────────────────────── */
    .contact-inner {
      display: grid;
      grid-template-columns: 1fr 1.4fr;
      gap: 4rem;
      max-width: 1200px;
      margin: 0 auto;
    }
    .contact-info { display: flex; flex-direction: column; gap: 2rem; }
    .contact-info h3 {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 2rem;
      text-transform: uppercase;
    }
    .contact-info > p { line-height: 1.8; }
    .contact-detail {
      display: flex;
      gap: 1rem;
      align-items: flex-start;
    }
    .contact-detail-icon {
      width: 44px;
      height: 44px;
      background: rgba(212,97,26,0.1);
      border: 1px solid rgba(212,97,26,0.2);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }
    .contact-detail-icon svg {
      width: 18px;
      height: 18px;
      stroke: var(--accent);
      fill: none;
      stroke-width: 1.5;
      stroke-linecap: round;
      stroke-linejoin: round;
    }
    .contact-detail-text strong {
      display: block;
      font-size: 0.78rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--text3);
      font-weight: 600;
      margin-bottom: 0.2rem;
    }
    .contact-detail-text span { font-size: 0.9rem; color: var(--text); }

    .map-placeholder {
      border-radius: var(--radius-lg);
      overflow: hidden;
      height: 200px;
      background: var(--bg3);
      border: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      gap: 0.75rem;
      color: var(--text3);
      font-size: 0.85rem;
    }
    .map-placeholder svg {
      width: 28px;
      height: 28px;
      stroke: var(--text3);
      fill: none;
      stroke-width: 1.5;
      stroke-linecap: round;
      stroke-linejoin: round;
    }

    /* Contact Form */
    .contact-form-wrap {
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 2.5rem;
    }
    .contact-form-wrap h4 {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 1.5rem;
      text-transform: uppercase;
      margin-bottom: 0.5rem;
    }
    .contact-form-wrap > p { font-size: 0.88rem; margin-bottom: 2rem; }

    .form-group { margin-bottom: 1.25rem; }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    label {
      display: block;
      font-size: 0.78rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      font-weight: 600;
      color: var(--text2);
      margin-bottom: 0.4rem;
    }
    input, select, textarea {
      width: 100%;
      background: var(--bg3);
      border: 1.5px solid var(--border);
      border-radius: var(--radius);
      padding: 0.75rem 1rem;
      color: var(--text);
      font-family: 'Inter', sans-serif;
      font-size: 0.9rem;
      transition: border-color var(--transition);
      outline: none;
    }
    input:focus, select:focus, textarea:focus { border-color: var(--accent); }
    select { appearance: none; cursor: pointer; }
    textarea { resize: vertical; min-height: 120px; }
    input::placeholder, textarea::placeholder { color: var(--text3); }
    select option { background: var(--bg2); }

    .form-submit {
      margin-top: 1.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      flex-wrap: wrap;
    }
    .form-note { font-size: 0.78rem; color: var(--text3); }

    .form-success {
      display: none;
      text-align: center;
      padding: 3rem 1rem;
    }
    .form-success .success-icon {
      width: 56px;
      height: 56px;
      background: rgba(212,97,26,0.1);
      border: 1px solid rgba(212,97,26,0.3);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 1.25rem;
    }
    .form-success .success-icon svg {
      width: 26px;
      height: 26px;
      stroke: var(--accent);
      fill: none;
      stroke-width: 2;
      stroke-linecap: round;
      stroke-linejoin: round;
    }
    .form-success h4 { font-family: 'Barlow Condensed', sans-serif; font-size: 1.5rem; text-transform: uppercase; color: var(--white); margin-bottom: 0.5rem; }
    .form-success p { font-size: 0.9rem; }

    /* ─── FOOTER ─────────────────────────────────────────────── */
    footer {
      background: var(--bg2);
      border-top: 1px solid var(--border);
      padding: 4rem 5% 2rem;
    }
    .footer-inner { max-width: 1200px; margin: 0 auto; }
    .footer-top {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 3rem;
      margin-bottom: 3rem;
      padding-bottom: 3rem;
      border-bottom: 1px solid var(--border);
    }
    .footer-brand p { font-size: 0.85rem; margin-top: 1rem; line-height: 1.7; max-width: 280px; }
    .footer-col h5 {
      font-family: 'Barlow Condensed', sans-serif;
      font-size: 0.85rem;
      font-weight: 700;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--white);
      margin-bottom: 1rem;
    }
    .footer-col ul { display: flex; flex-direction: column; gap: 0.6rem; }
    .footer-col li a {
      font-size: 0.85rem;
      color: var(--text2);
      transition: color var(--transition);
      cursor: pointer;
    }
    .footer-col li a:hover { color: var(--accent); }
    .footer-bottom {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      flex-wrap: wrap;
    }
    .footer-bottom p { font-size: 0.8rem; color: var(--text3); }
    .footer-bottom a { color: var(--accent); cursor: pointer; }
    .certifications { display: flex; gap: 0.75rem; flex-wrap: wrap; margin-top: 1rem; }
    .cert-badge {
      background: rgba(212,97,26,0.08);
      border: 1px solid rgba(212,97,26,0.2);
      border-radius: 4px;
      padding: 0.25rem 0.65rem;
      font-size: 0.7rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--accent);
      font-weight: 600;
    }

    /* ─── ANIMATIONS ─────────────────────────────────────────── */
    .fade-up {
      opacity: 0;
      transform: translateY(28px);
      transition: opacity 0.55s ease, transform 0.55s ease;
    }
    .fade-up.visible { opacity: 1; transform: translateY(0); }
    .fade-up:nth-child(2) { transition-delay: 0.08s; }
    .fade-up:nth-child(3) { transition-delay: 0.16s; }
    .fade-up:nth-child(4) { transition-delay: 0.24s; }
    .fade-up:nth-child(5) { transition-delay: 0.32s; }
    .fade-up:nth-child(6) { transition-delay: 0.40s; }

    /* ─── RESPONSIVE ─────────────────────────────────────────── */
    @media (max-width: 1024px) {
      .stats-grid { grid-template-columns: repeat(2, 1fr); }
      .stat-item:nth-child(2) { border-right: none; }
      .stat-item:nth-child(3) { border-top: 1px solid var(--border); }
      .services-grid { grid-template-columns: repeat(2, 1fr); }
      .why-inner { grid-template-columns: 1fr; gap: 3rem; }
      .why-img { aspect-ratio: 16/9; }
      .about-story { grid-template-columns: 1fr; gap: 3rem; }
      .about-story-img { aspect-ratio: 16/9; }
      .values-grid { grid-template-columns: repeat(2, 1fr); }
      .accreditations { grid-template-columns: repeat(2, 1fr); }
      .footer-top { grid-template-columns: 1fr 1fr; }
      .contact-inner { grid-template-columns: 1fr; }
      .service-full-item { grid-template-columns: 1fr; direction: ltr !important; }
      .service-full-item.reverse { direction: ltr !important; }
    }
    @media (max-width: 768px) {
      section { padding: 4rem 5%; }
      .nav-links, nav > .btn { display: none; }
      .hamburger { display: flex; }
      .hero { min-height: 95vh; }
      .testimonials-grid { grid-template-columns: 1fr; }
      .gallery-grid { grid-template-columns: repeat(2, 1fr); }
      .gallery-item.wide { grid-column: span 1; aspect-ratio: 4/3; }
      .values-grid { grid-template-columns: 1fr 1fr; }
      .accreditations { grid-template-columns: 1fr 1fr; }
      .footer-top { grid-template-columns: 1fr; gap: 2rem; }
      .form-row { grid-template-columns: 1fr; }
    }
    @media (max-width: 480px) {
      h1 { font-size: 2.4rem; }
      .services-grid { grid-template-columns: 1fr; }
      .stats-grid { grid-template-columns: 1fr 1fr; }
      .gallery-grid { grid-template-columns: 1fr; }
      .gallery-item.wide { grid-column: span 1; }
      .values-grid { grid-template-columns: 1fr; }
      .accreditations { grid-template-columns: 1fr; }
      .hero-ctas { flex-direction: column; }
      .hero-ctas .btn { width: 100%; justify-content: center; }
    }
  </style>
</head>
<body>

  <!-- ─────────────── NAVIGATION ─────────────── -->
  <nav id="main-nav">
    <div class="nav-logo" onclick="showPage('home')">
      <span class="wordmark">Ridge<span>line</span></span>
      <span class="sub">Roofing &amp; Construction</span>
    </div>
    <div class="nav-links">
      <a onclick="showPage('home')" data-page="home" class="active">Home</a>
      <a onclick="showPage('services')" data-page="services">Services</a>
      <a onclick="showPage('about')" data-page="about">About</a>
      <a onclick="showPage('gallery')" data-page="gallery">Gallery</a>
      <a onclick="showPage('contact')" data-page="contact">Contact</a>
    </div>
    <button class="btn btn-primary" onclick="showPage('contact')">Get a Free Quote</button>
    <div class="hamburger" id="hamburger" onclick="toggleMobile()">
      <span></span><span></span><span></span>
    </div>
  </nav>

  <!-- Mobile Menu -->
  <div class="mobile-menu" id="mobile-menu">
    <a onclick="showPage('home');closeMobile()">Home</a>
    <a onclick="showPage('services');closeMobile()">Services</a>
    <a onclick="showPage('about');closeMobile()">About</a>
    <a onclick="showPage('gallery');closeMobile()">Gallery</a>
    <a onclick="showPage('contact');closeMobile()">Contact</a>
    <button class="btn btn-primary" style="width:fit-content" onclick="showPage('contact');closeMobile()">Get a Free Quote</button>
  </div>


  <!-- ════════════════════════════════════════
       HOME PAGE
  ════════════════════════════════════════ -->
  <div id="page-home" class="page active">

    <!-- HERO -->
    <section class="hero">
      <div class="hero-bg"></div>
      <div class="hero-overlay"></div>
      <div class="hero-content">
        <div class="hero-badge">
          <div class="hero-badge-dot"></div>
          Manchester's Trusted Roofers Since 2003
        </div>
        <h1>Built Right.<br><span>Weatherproof.</span><br>Guaranteed.</h1>
        <p>From pitched roofs and flat systems to emergency call-outs — Ridgeline has protected Manchester homes and businesses for over 20 years. No subcontractors. No shortcuts.</p>
        <div class="hero-ctas">
          <button class="btn btn-primary btn-lg" onclick="showPage('contact')">Get a Free Quote</button>
          <button class="btn btn-outline btn-lg" onclick="showPage('gallery')">See Our Work</button>
        </div>
      </div>
      <div class="scroll-hint">Scroll</div>
    </section>

    <!-- STATS BAR -->
    <div class="stats-bar">
      <div class="stats-grid">
        <div class="stat-item">
          <div class="stat-num" data-count="20">0</div>
          <div class="stat-label">Years in Business</div>
        </div>
        <div class="stat-item">
          <div class="stat-num" data-count="500">0</div>
          <div class="stat-label">Roofs Completed</div>
        </div>
        <div class="stat-item">
          <div class="stat-num" style="font-size:2rem">24/7</div>
          <div class="stat-label">Emergency Cover</div>
        </div>
        <div class="stat-item">
          <div class="stat-num" style="font-size:2rem">10yr</div>
          <div class="stat-label">Workmanship Guarantee</div>
        </div>
      </div>
    </div>

    <!-- SERVICES OVERVIEW -->
    <section style="background:var(--bg)">
      <div class="container">
        <div class="section-head">
          <p class="label">What We Do</p>
          <h2>Full-Range Roofing<br>Across Greater Manchester</h2>
          <p>Every job is handled by our own team — not outsourced. Whether it's a single tile or a full commercial roof, you deal with Ridgeline from start to finish.</p>
        </div>
        <div class="services-grid">
          <div class="service-card fade-up" onclick="showPage('services')">
            <div class="service-icon">
              <!-- house -->
              <svg viewBox="0 0 24 24"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
            </div>
            <h4>Pitched Roofing</h4>
            <p>Tile and slate repairs, full strip-and-relay, and new-build installs. We work with all pitched roof systems on both period and modern properties.</p>
          </div>
          <div class="service-card fade-up" onclick="showPage('services')">
            <div class="service-icon">
              <!-- layers -->
              <svg viewBox="0 0 24 24"><polygon points="12 2 2 7 12 12 22 7 12 2"/><polyline points="2 17 12 22 22 17"/><polyline points="2 12 12 17 22 12"/></svg>
            </div>
            <h4>Flat Roofing</h4>
            <p>EPDM rubber, GRP fibreglass, and torch-on felt systems. Long-lasting solutions with proper drainage design and a 10-year guarantee on all materials.</p>
          </div>
          <div class="service-card fade-up" onclick="showPage('services')">
            <div class="service-icon">
              <!-- droplet -->
              <svg viewBox="0 0 24 24"><path d="M12 2.69l5.66 5.66a8 8 0 11-11.31 0z"/></svg>
            </div>
            <h4>Guttering &amp; Fascias</h4>
            <p>Full uPVC replacement for gutters, fascias, soffits, and downpipes. We clear, repair, or replace — whatever the job needs.</p>
          </div>
          <div class="service-card fade-up" onclick="showPage('services')">
            <div class="service-icon">
              <!-- tool/wrench -->
              <svg viewBox="0 0 24 24"><path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z"/></svg>
            </div>
            <h4>Chimney &amp; Leadwork</h4>
            <p>Chimney repointing, stack repairs, lead flashing, and valley work. We fix the areas other roofers skip over — the ones that cause the leaks.</p>
          </div>
          <div class="service-card fade-up" onclick="showPage('services')">
            <div class="service-icon">
              <!-- zap -->
              <svg viewBox="0 0 24 24"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
            </div>
            <h4>Emergency Repairs</h4>
            <p>Storm damage, sudden leaks, and structural failures. We respond fast, contain the problem, and agree on permanent repairs once the situation is safe.</p>
          </div>
          <div class="service-card fade-up" onclick="showPage('services')">
            <div class="service-icon">
              <!-- grid/building -->
              <svg viewBox="0 0 24 24"><rect x="3" y="3" width="7" height="7"/><rect x="14" y="3" width="7" height="7"/><rect x="14" y="14" width="7" height="7"/><rect x="3" y="14" width="7" height="7"/></svg>
            </div>
            <h4>Commercial Roofing</h4>
            <p>Industrial and commercial flat roofing for warehouses, offices, and retail units across Greater Manchester. Single-ply, built-up, and liquid systems available.</p>
          </div>
        </div>
        <div style="text-align:center;margin-top:2.5rem">
          <button class="btn btn-outline" onclick="showPage('services')">View All Services</button>
        </div>
      </div>
    </section>

    <!-- WHY RIDGELINE -->
    <section style="background:var(--bg)">
      <div class="why-inner">
        <div class="why-img fade-up">
          <img
            src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=800&q=80"
            alt="Ridgeline team at work"
            onerror="this.parentElement.style.background='var(--bg3)'"
          />
          <div class="why-badge">
            <div class="num">500+</div>
            <div class="txt">Projects Completed</div>
          </div>
        </div>
        <div>
          <p class="label">Why Choose Ridgeline</p>
          <h2 style="text-transform:uppercase;margin:0.75rem 0 1rem">Built on<br>Reputation</h2>
          <p style="line-height:1.8">We've been roofing in Manchester since 2003. Most of our work comes from referrals — homeowners who trusted us, then told their neighbours. That's the kind of reputation we protect with every job.</p>
          <div class="why-points">
            <div class="why-point fade-up">
              <div class="why-point-icon">
                <svg viewBox="0 0 24 24"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg>
              </div>
              <div class="why-point-text">
                <h4>Your Own Team — Not Subcontractors</h4>
                <p>Every roofer on your job is a Ridgeline employee. We don't broker work to unknown trades. Same faces from start to finish.</p>
              </div>
            </div>
            <div class="why-point fade-up">
              <div class="why-point-icon">
                <svg viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
              </div>
              <div class="why-point-text">
                <h4>Written Quote, Fixed Price</h4>
                <p>You get an itemised written quote before any work starts. If something changes, we discuss it before we invoice — not after.</p>
              </div>
            </div>
            <div class="why-point fade-up">
              <div class="why-point-icon">
                <svg viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
              </div>
              <div class="why-point-text">
                <h4>10-Year Workmanship Guarantee</h4>
                <p>All Ridgeline work carries a 10-year guarantee. Fully insured, NFRC registered, and independently backed. No small print.</p>
              </div>
            </div>
            <div class="why-point fade-up">
              <div class="why-point-icon">
                <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
              </div>
              <div class="why-point-text">
                <h4>Free Quote Within 48 Hours</h4>
                <p>No-obligation site inspection and written quote within two working days. Most jobs in the Manchester area get same-week visits.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="testimonials-section">
      <div class="container">
        <div class="section-head">
          <p class="label">What Our Customers Say</p>
          <h2>Real Manchester<br>Homeowners</h2>
        </div>
        <div class="testimonials-grid">
          <div class="testimonial-card fade-up">
            <div class="stars">
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
            </div>
            <p>"Used Ridgeline after storm damage last October. They were on site within 24 hours, sorted the emergency fix the same day, and replaced the full section of roof the following week. Excellent from start to finish."</p>
            <div class="t-author">
              <div class="t-avatar">PH</div>
              <div>
                <div class="t-name">Paul Hargreaves</div>
                <div class="t-loc">Chorlton, Manchester</div>
              </div>
            </div>
          </div>
          <div class="testimonial-card fade-up">
            <div class="stars">
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
            </div>
            <p>"Had three quotes for a full roof replacement. Ridgeline weren't the cheapest, but their quote was the most detailed and the only one that actually explained what they were doing. Work was done in four days, site left spotless."</p>
            <div class="t-author">
              <div class="t-avatar">SK</div>
              <div>
                <div class="t-name">Sandra Khan</div>
                <div class="t-loc">Didsbury, Manchester</div>
              </div>
            </div>
          </div>
          <div class="testimonial-card fade-up">
            <div class="stars">
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
              <svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg>
            </div>
            <p>"They replaced our guttering and fascias — the team were professional, tidy, and finished a day ahead of schedule. We've already recommended them to two people on our street. Will use again without question."</p>
            <div class="t-author">
              <div class="t-avatar">TO</div>
              <div>
                <div class="t-name">Tom &amp; Claire O'Brien</div>
                <div class="t-loc">Salford, Greater Manchester</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA BANNER -->
    <div class="cta-banner">
      <div class="container">
        <h2>Got a Roofing Problem?<br>Let's Fix It.</h2>
        <p>Free, no-obligation quote. Site visit within 48 hours. We cover all of Greater Manchester.</p>
        <button class="btn btn-white btn-lg" onclick="showPage('contact')">Get a Free Quote</button>
      </div>
    </div>

  </div><!-- /page-home -->


  <!-- ════════════════════════════════════════
       SERVICES PAGE
  ════════════════════════════════════════ -->
  <div id="page-services" class="page">
    <div class="page-hero">
      <p class="label">What We Offer</p>
      <h1>Our Services</h1>
      <p>Full-range roofing and construction for Manchester homes and businesses. All work carried out by our own team — not subcontracted out.</p>
    </div>

    <div style="background:var(--bg)">
      <div class="services-full">

        <div class="service-full-item">
          <div class="service-full-img">
            <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?auto=format&fit=crop&w=800&q=80" alt="Pitched roofing" onerror="this.parentElement.style.background='var(--bg3)'" />
          </div>
          <div class="service-full-body">
            <p class="label">Service 01</p>
            <h3>Pitched Roofing</h3>
            <p>Whether you need a single tile replacing or a full strip-and-relay, our pitched roofing team handles it with the same level of care. We work on period terraces, semi-detached homes, and new builds across Greater Manchester.</p>
            <ul class="service-list">
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Full roof replacements — concrete and clay tiles, natural slate</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Partial repairs and tile matching on older properties</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Roof inspections and written condition reports</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Moss removal and treatment to extend roof life</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Ridge, hip, and valley restoration</li>
            </ul>
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Quote</button>
          </div>
        </div>

        <div class="service-full-item reverse">
          <div class="service-full-img">
            <img src="https://images.unsplash.com/photo-1486325212027-8081e485255e?auto=format&fit=crop&w=800&q=80" alt="Flat roofing" onerror="this.parentElement.style.background='var(--bg3)'" />
          </div>
          <div class="service-full-body">
            <p class="label">Service 02</p>
            <h3>Flat Roofing</h3>
            <p>We install long-life flat roof systems that are properly designed for drainage and weather resistance. No temporary fixes — only systems we're confident enough to guarantee for 10 years.</p>
            <ul class="service-list">
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>EPDM rubber roofing — durable, lightweight, 50+ year lifespan</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>GRP fibreglass — seamless and ideal for complex shapes</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Torch-on felt — cost-effective for lower-pitch applications</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Flat-to-pitched conversions</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Drainage design and outlet installation</li>
            </ul>
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Quote</button>
          </div>
        </div>

        <div class="service-full-item">
          <div class="service-full-img">
            <img src="https://images.unsplash.com/photo-1570129477492-45c003edd2be?auto=format&fit=crop&w=800&q=80" alt="Guttering and fascias" onerror="this.parentElement.style.background='var(--bg3)'" />
          </div>
          <div class="service-full-body">
            <p class="label">Service 03</p>
            <h3>Guttering &amp; Fascias</h3>
            <p>Faulty guttering causes more damage to homes than most people realise. Overflows erode brickwork, saturate walls, and rot fascia boards over time. We replace or repair it properly, first time.</p>
            <ul class="service-list">
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Full uPVC gutter replacement in any profile or colour</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Fascia and soffit replacement — white, black, or woodgrain finish</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Downpipe replacement and re-routing</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Gutter clearing and maintenance contracts</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Dry verge and dry ridge installation</li>
            </ul>
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Quote</button>
          </div>
        </div>

        <div class="service-full-item reverse">
          <div class="service-full-img">
            <img src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=800&q=80" alt="Chimney and leadwork" onerror="this.parentElement.style.background='var(--bg3)'" />
          </div>
          <div class="service-full-body">
            <p class="label">Service 04</p>
            <h3>Chimney &amp; Leadwork</h3>
            <p>Chimneys and lead flashings are the most common source of roof leaks — and the most frequently missed during basic repairs. Our team specialises in the detail work that actually solves the problem.</p>
            <ul class="service-list">
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Chimney stack repointing and render repair</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Lead flashing replacement and step flashing</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Chimney pot re-bedding and cowl installation</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Valley lead replacement and re-dressing</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Full chimney removal if decommissioned</li>
            </ul>
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Quote</button>
          </div>
        </div>

        <div class="service-full-item">
          <div class="service-full-img">
            <img src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=800&q=80" alt="Emergency repairs" onerror="this.parentElement.style.background='var(--bg3)'" />
          </div>
          <div class="service-full-body">
            <p class="label">Service 05</p>
            <h3>Emergency Repairs</h3>
            <p>Storm damage doesn't keep office hours. We have an emergency response team available 24/7 to make your property safe and watertight. We'll contain the problem first, then discuss permanent repairs once the situation is stable.</p>
            <ul class="service-list">
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>24/7 storm damage response across Greater Manchester</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Emergency tarpaulin and temporary cover installation</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Same-day callouts for active leaks and structural damage</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Insurance report and photographic evidence provided</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Priority booking for permanent follow-up work</li>
            </ul>
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Quote</button>
          </div>
        </div>

        <div class="service-full-item reverse">
          <div class="service-full-img">
            <img src="https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&w=800&q=80" alt="Commercial roofing" onerror="this.parentElement.style.background='var(--bg3)'" />
          </div>
          <div class="service-full-body">
            <p class="label">Service 06</p>
            <h3>Commercial Roofing</h3>
            <p>We work with businesses, landlords, and property managers across Greater Manchester on commercial flat roofing projects. We manage the project and minimise disruption to your operations.</p>
            <ul class="service-list">
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Single-ply membrane systems (TPO, PVC, EPDM)</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Built-up roofing (BUR) for large commercial spans</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Liquid-applied coatings for refurbishment projects</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Planned maintenance contracts and inspection schedules</li>
              <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Out-of-hours working to avoid business disruption</li>
            </ul>
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Quote</button>
          </div>
        </div>

      </div>
    </div>

    <div class="cta-banner">
      <h2>Not Sure Which Service You Need?</h2>
      <p>Call us or send a message and we'll advise you honestly — even if that means recommending a smaller, cheaper fix.</p>
      <button class="btn btn-white btn-lg" onclick="showPage('contact')">Talk to Our Team</button>
    </div>
  </div><!-- /page-services -->


  <!-- ════════════════════════════════════════
       ABOUT PAGE
  ════════════════════════════════════════ -->
  <div id="page-about" class="page">
    <div class="page-hero">
      <p class="label">Our Story</p>
      <h1>About Ridgeline</h1>
      <p>A Manchester roofing company built on honest work, proper materials, and the belief that a good job should speak for itself.</p>
    </div>

    <section style="background:var(--bg)">
      <div class="about-story">
        <div class="about-story-img fade-up">
          <img src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=800&q=80" alt="Ridgeline team" onerror="this.parentElement.style.background='var(--bg3)'" />
        </div>
        <div class="about-story-text">
          <p class="label">Est. 2003 — Manchester</p>
          <h2>Twenty Years of Protecting Manchester Rooftops</h2>
          <p>Ridgeline was founded in 2003 by David Holt, a Manchester-born roofer who wanted to do things differently. No subcontracting. No disappearing after the deposit. No padding out quotes with work that isn't needed.</p>
          <p>Today we're a team of 18, and the principles haven't changed. Every job is carried out by Ridgeline employees. Every quote is itemised. Every project comes with a written guarantee. Over 90% of our new work comes from referrals — homeowners who were happy, and told someone about it.</p>
          <p>We cover all of Greater Manchester, from Salford and Trafford to Stockport, Oldham, and Bury. If you're on our patch, we can be with you quickly — usually within 48 hours for a no-obligation quote.</p>
          <div style="margin-top:1.5rem;display:flex;gap:1rem;flex-wrap:wrap">
            <button class="btn btn-primary" onclick="showPage('contact')">Get a Free Quote</button>
            <button class="btn btn-outline" onclick="showPage('gallery')">See Our Work</button>
          </div>
        </div>
      </div>
    </section>

    <section class="values-section">
      <div class="container">
        <div class="section-head">
          <p class="label">How We Work</p>
          <h2>What Makes Us Different</h2>
        </div>
        <div class="values-grid">
          <div class="value-card fade-up">
            <div class="value-icon">
              <svg viewBox="0 0 24 24"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg>
            </div>
            <h4>No Subcontracting</h4>
            <p>Your job is carried out by our team, not handed off to someone we've never worked with. Same faces, same standards, every time.</p>
          </div>
          <div class="value-card fade-up">
            <div class="value-icon">
              <svg viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/></svg>
            </div>
            <h4>Transparent Quotes</h4>
            <p>Every quote is itemised in writing. You'll know exactly what you're paying for before anything starts — and the price doesn't change unless you ask for something extra.</p>
          </div>
          <div class="value-card fade-up">
            <div class="value-icon">
              <svg viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
            </div>
            <h4>10-Year Guarantee</h4>
            <p>All workmanship is guaranteed for 10 years. Fully insured and NFRC registered. If something fails, we fix it — no questions asked.</p>
          </div>
          <div class="value-card fade-up">
            <div class="value-icon">
              <svg viewBox="0 0 24 24"><polyline points="9 11 12 14 22 4"/><path d="M21 12v7a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h11"/></svg>
            </div>
            <h4>Clean Sites</h4>
            <p>We clear up at the end of every working day. Living through a roofing job is disruptive enough — a tidy site is the least we can do.</p>
          </div>
        </div>
      </div>
    </section>

    <section style="background:var(--bg)">
      <div class="container">
        <div class="section-head">
          <p class="label">Accreditations &amp; Insurance</p>
          <h2>Registered, Insured<br>&amp; Certified</h2>
          <p>We hold the industry certifications that matter — not just for compliance, but because they're the standard we hold ourselves to.</p>
        </div>
        <div class="accreditations">
          <div class="accred-card fade-up">
            <span class="accred-tag">Industry</span>
            <h4>NFRC Member</h4>
            <p>National Federation of Roofing Contractors. The UK's largest roofing trade body, setting standards for quality and safety.</p>
          </div>
          <div class="accred-card fade-up">
            <span class="accred-tag">Insurance</span>
            <h4>Fully Public Liability Insured</h4>
            <p>5 million pounds public liability insurance on all jobs. You're covered from day one to completion and beyond.</p>
          </div>
          <div class="accred-card fade-up">
            <span class="accred-tag">Health &amp; Safety</span>
            <h4>SSIP Certified</h4>
            <p>Safety Schemes in Procurement — independently verified health and safety management. Required for all commercial roofing work.</p>
          </div>
          <div class="accred-card fade-up">
            <span class="accred-tag">Manufacturer</span>
            <h4>Approved Installer</h4>
            <p>Certified installer for leading flat roofing membrane manufacturers, allowing us to pass extended manufacturer warranties directly to you.</p>
          </div>
        </div>
      </div>
    </section>

    <div class="cta-banner">
      <h2>Ready to Get Started?</h2>
      <p>Free site visit and written quote within 48 hours. No call centres — you'll speak to someone who actually knows roofing.</p>
      <button class="btn btn-white btn-lg" onclick="showPage('contact')">Get a Free Quote</button>
    </div>
  </div><!-- /page-about -->


  <!-- ════════════════════════════════════════
       GALLERY PAGE
  ════════════════════════════════════════ -->
  <div id="page-gallery" class="page">
    <div class="page-hero">
      <p class="label">Our Work</p>
      <h1>Project Gallery</h1>
      <p>A selection of completed projects across Greater Manchester. Residential, commercial, pitched, flat, and emergency — all carried out by our own team.</p>
    </div>

    <section style="background:var(--bg)">
      <div class="container">
        <div class="gallery-filter">
          <button class="filter-btn active" data-filter="all">All Projects</button>
          <button class="filter-btn" data-filter="pitched">Pitched Roofing</button>
          <button class="filter-btn" data-filter="flat">Flat Roofing</button>
          <button class="filter-btn" data-filter="guttering">Guttering</button>
          <button class="filter-btn" data-filter="commercial">Commercial</button>
        </div>

        <div class="gallery-grid">
          <div class="gallery-item wide" data-cat="pitched">
            <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?auto=format&fit=crop&w=1200&q=80" alt="Full roof replacement Didsbury" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>Full Roof Replacement</h4><span>Pitched Roofing — Didsbury, Manchester</span></div>
            </div>
          </div>
          <div class="gallery-item" data-cat="flat">
            <img src="https://images.unsplash.com/photo-1486325212027-8081e485255e?auto=format&fit=crop&w=800&q=80" alt="EPDM flat roof Salford" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>EPDM Flat Roof</h4><span>Flat Roofing — Salford</span></div>
            </div>
          </div>
          <div class="gallery-item" data-cat="commercial">
            <img src="https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&w=800&q=80" alt="Commercial flat roof Trafford" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>Commercial Flat Roof</h4><span>Commercial — Trafford Park</span></div>
            </div>
          </div>
          <div class="gallery-item" data-cat="pitched">
            <img src="https://images.unsplash.com/photo-1513584684374-8bab748fbf90?auto=format&fit=crop&w=800&q=80" alt="Slate roof Chorlton" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>Natural Slate Replacement</h4><span>Pitched Roofing — Chorlton</span></div>
            </div>
          </div>
          <div class="gallery-item wide" data-cat="guttering">
            <img src="https://images.unsplash.com/photo-1570129477492-45c003edd2be?auto=format&fit=crop&w=1200&q=80" alt="Full fascia and guttering Stockport" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>Full Fascia &amp; Guttering Replacement</h4><span>Guttering — Stockport</span></div>
            </div>
          </div>
          <div class="gallery-item" data-cat="flat">
            <img src="https://images.unsplash.com/photo-1591588582259-e675bd2e6088?auto=format&fit=crop&w=800&q=80" alt="GRP fibreglass Oldham" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>GRP Fibreglass System</h4><span>Flat Roofing — Oldham</span></div>
            </div>
          </div>
          <div class="gallery-item" data-cat="pitched">
            <img src="https://images.unsplash.com/photo-1600607687920-4e2a09cf159d?auto=format&fit=crop&w=800&q=80" alt="Chimney repoint Bury" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>Chimney Repoint &amp; Leadwork</h4><span>Chimney &amp; Lead — Bury</span></div>
            </div>
          </div>
          <div class="gallery-item" data-cat="commercial">
            <img src="https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=800&q=80" alt="Emergency storm repair Eccles" onerror="this.parentElement.style.background='var(--bg3)'" />
            <div class="gallery-overlay">
              <div class="gallery-overlay-text"><h4>Emergency Storm Repair</h4><span>Emergency — Eccles</span></div>
            </div>
          </div>
        </div>

        <div style="text-align:center;margin-top:3rem">
          <p style="margin-bottom:1.5rem;font-size:0.9rem">Want to see work in a specific area or roof type?</p>
          <button class="btn btn-primary btn-lg" onclick="showPage('contact')">Get a Free Quote for Your Roof</button>
        </div>
      </div>
    </section>
  </div><!-- /page-gallery -->


  <!-- ════════════════════════════════════════
       CONTACT PAGE
  ════════════════════════════════════════ -->
  <div id="page-contact" class="page">
    <div class="page-hero">
      <p class="label">Get in Touch</p>
      <h1>Free Quote &amp;<br>Site Visit</h1>
      <p>No call centres. No waiting on hold. Fill in the form and someone from our team will be in touch within one working day.</p>
    </div>

    <section style="background:var(--bg)">
      <div class="contact-inner">
        <div class="contact-info">
          <div>
            <h3>Talk to a Real Roofer</h3>
            <p style="margin-top:0.75rem;line-height:1.8">We're a Manchester team — if you call or message, you'll speak with someone who can actually answer your question. No scripts, no call handlers.</p>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">
              <svg viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.09 9.8a19.79 19.79 0 01-3.07-8.67A2 2 0 012 1h3a2 2 0 012 1.72 12.84 12.84 0 00.7 2.81 2 2 0 01-.45 2.11L6.09 8.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45 12.84 12.84 0 002.81.7A2 2 0 0122 16.92z"/></svg>
            </div>
            <div class="contact-detail-text">
              <strong>Phone</strong>
              <span>0161 429 8830</span>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">
              <svg viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            </div>
            <div class="contact-detail-text">
              <strong>Email</strong>
              <span>info@ridglineroofing.co.uk</span>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">
              <svg viewBox="0 0 24 24"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
            </div>
            <div class="contact-detail-text">
              <strong>Address</strong>
              <span>Unit 7, Trafford Park<br>Manchester, M17 1BX</span>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">
              <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
            </div>
            <div class="contact-detail-text">
              <strong>Office Hours</strong>
              <span>Mon–Fri: 7:00am – 6:00pm<br>Sat: 8:00am – 1:00pm</span>
            </div>
          </div>
          <div class="contact-detail">
            <div class="contact-detail-icon">
              <svg viewBox="0 0 24 24"><polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2"/></svg>
            </div>
            <div class="contact-detail-text">
              <strong>Emergency Line</strong>
              <span>Available 24/7 for storm damage and active leaks</span>
            </div>
          </div>
          <div class="map-placeholder">
            <svg viewBox="0 0 24 24"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
            <p>Trafford Park, Manchester M17</p>
            <p style="font-size:0.78rem;color:var(--text3)">Covering all of Greater Manchester</p>
          </div>
        </div>

        <div class="contact-form-wrap">
          <h4>Request a Free Quote</h4>
          <p>Site visit within 48 hours. Written quote included. No obligation.</p>
          <form id="contact-form">
            <div class="form-row">
              <div class="form-group">
                <label for="fname">First Name</label>
                <input type="text" id="fname" placeholder="David" required />
              </div>
              <div class="form-group">
                <label for="lname">Last Name</label>
                <input type="text" id="lname" placeholder="Holt" required />
              </div>
            </div>
            <div class="form-row">
              <div class="form-group">
                <label for="phone">Phone Number</label>
                <input type="tel" id="phone" placeholder="0161 000 0000" required />
              </div>
              <div class="form-group">
                <label for="email">Email Address</label>
                <input type="email" id="email" placeholder="your@email.co.uk" />
              </div>
            </div>
            <div class="form-group">
              <label for="service">Service Required</label>
              <select id="service">
                <option value="">Select a service…</option>
                <option>Pitched Roofing</option>
                <option>Flat Roofing</option>
                <option>Guttering &amp; Fascias</option>
                <option>Chimney &amp; Leadwork</option>
                <option>Emergency Repair</option>
                <option>Commercial Roofing</option>
                <option>Not sure — need advice</option>
              </select>
            </div>
            <div class="form-group">
              <label for="address">Property Address</label>
              <input type="text" id="address" placeholder="123 High Street, Manchester" />
            </div>
            <div class="form-group">
              <label for="message">Tell Us About the Job</label>
              <textarea id="message" placeholder="Describe the issue or project as best you can — any details help us prepare for the site visit."></textarea>
            </div>
            <div class="form-submit">
              <p class="form-note">We respond within one working day. Emergency? Call 0161 429 8830.</p>
              <button type="submit" class="btn btn-primary btn-lg">Send Request</button>
            </div>
          </form>
          <div class="form-success" id="form-success">
            <div class="success-icon">
              <svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>
            </div>
            <h4>Request Received</h4>
            <p>Thanks — we'll be in touch within one working day to arrange your free site visit and quote.</p>
          </div>
        </div>
      </div>
    </section>
  </div><!-- /page-contact -->


  <!-- ─────────────── FOOTER ─────────────── -->
  <footer>
    <div class="footer-inner">
      <div class="footer-top">
        <div class="footer-brand">
          <div class="nav-logo" style="cursor:default">
            <span class="wordmark">Ridge<span>line</span></span>
            <span class="sub">Roofing &amp; Construction</span>
          </div>
          <p>Manchester's trusted roofing team since 2003. Pitched, flat, guttering, chimneys, and emergency repairs — all handled by our own crew.</p>
          <div class="certifications">
            <span class="cert-badge">NFRC</span>
            <span class="cert-badge">SSIP</span>
            <span class="cert-badge">Fully Insured</span>
            <span class="cert-badge">10yr Guarantee</span>
          </div>
        </div>
        <div class="footer-col">
          <h5>Services</h5>
          <ul>
            <li><a onclick="showPage('services')">Pitched Roofing</a></li>
            <li><a onclick="showPage('services')">Flat Roofing</a></li>
            <li><a onclick="showPage('services')">Guttering &amp; Fascias</a></li>
            <li><a onclick="showPage('services')">Chimney &amp; Leadwork</a></li>
            <li><a onclick="showPage('services')">Emergency Repairs</a></li>
            <li><a onclick="showPage('services')">Commercial Roofing</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h5>Company</h5>
          <ul>
            <li><a onclick="showPage('home')">Home</a></li>
            <li><a onclick="showPage('about')">About Us</a></li>
            <li><a onclick="showPage('gallery')">Gallery</a></li>
            <li><a onclick="showPage('contact')">Get a Quote</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h5>Contact</h5>
          <ul>
            <li><a>0161 429 8830</a></li>
            <li><a>info@ridglineroofing.co.uk</a></li>
            <li><a>Unit 7, Trafford Park, Manchester M17 1BX</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <p>2024 Ridgeline Roofing &amp; Construction Ltd. All rights reserved. Registered in England &amp; Wales.</p>
        <p>Site by <a onclick="showPage('home')">Kaira Agency</a></p>
      </div>
    </div>
  </footer>


  <!-- ─────────────── SCRIPTS ─────────────── -->
  <script>
    /* ── PAGE NAVIGATION ── */
    function showPage(id) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      const target = document.getElementById('page-' + id);
      if (target) target.classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
      document.querySelectorAll('.nav-links a').forEach(a => {
        a.classList.toggle('active', a.dataset.page === id);
      });
      setTimeout(initAnimations, 80);
    }

    /* ── NAV SCROLL EFFECT ── */
    window.addEventListener('scroll', () => {
      document.getElementById('main-nav').classList.toggle('scrolled', window.scrollY > 40);
    });

    /* ── MOBILE MENU ── */
    function toggleMobile() {
      document.getElementById('hamburger').classList.toggle('open');
      document.getElementById('mobile-menu').classList.toggle('open');
    }
    function closeMobile() {
      document.getElementById('hamburger').classList.remove('open');
      document.getElementById('mobile-menu').classList.remove('open');
    }

    /* ── SCROLL ANIMATIONS ── */
    function initAnimations() {
      const els = document.querySelectorAll('.fade-up:not(.visible)');
      if (!els.length) return;
      const obs = new IntersectionObserver((entries) => {
        entries.forEach(e => {
          if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); }
        });
      }, { threshold: 0.1 });
      els.forEach(el => obs.observe(el));
    }
    initAnimations();

    /* ── COUNTER ANIMATION ── */
    function animateCounters() {
      document.querySelectorAll('[data-count]').forEach(el => {
        const target = parseInt(el.dataset.count);
        let current = 0;
        const step = Math.ceil(target / 55);
        const timer = setInterval(() => {
          current = Math.min(current + step, target);
          el.textContent = current + '+';
          if (current >= target) clearInterval(timer);
        }, 18);
      });
    }
    const statsObs = new IntersectionObserver((entries) => {
      entries.forEach(e => { if (e.isIntersecting) { animateCounters(); statsObs.disconnect(); } });
    }, { threshold: 0.3 });
    const statsBar = document.querySelector('.stats-bar');
    if (statsBar) statsObs.observe(statsBar);

    /* ── GALLERY FILTER ── */
    document.querySelectorAll('.filter-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        const filter = btn.dataset.filter;
        document.querySelectorAll('.gallery-item').forEach(item => {
          item.style.display = (filter === 'all' || item.dataset.cat === filter) ? '' : 'none';
        });
      });
    });

    /* ── CONTACT FORM ── */
    document.getElementById('contact-form').addEventListener('submit', function(e) {
      e.preventDefault();
      this.style.display = 'none';
      document.getElementById('form-success').style.display = 'block';
    });
  </script>

</body>
</html>

