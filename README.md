# Veer
This is my portfolio web page. My name is Veer. I am a Mathematics and programming teacher/tutor.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Veer Sanjot | Teacher & Tutor</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --teal: #0D3B4A;
    --teal-mid: #1A5568;
    --teal-light: #2B7A8F;
    --gold: #C9A84C;
    --gold-light: #E8C97A;
    --ivory: #F7F4EF;
    --white: #FAFAF8;
    --slate: #4A6572;
    --slate-light: #8FA8B2;
    --text-dark: #1A2C33;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--ivory);
    color: var(--text-dark);
    min-height: 100vh;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    background: var(--teal);
    z-index: 1000;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2rem;
    height: 64px;
    box-shadow: 0 2px 16px rgba(13,59,74,0.35);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--gold);
    letter-spacing: 0.03em;
    cursor: pointer;
  }

  .nav-links {
    display: flex;
    gap: 0.25rem;
    list-style: none;
  }

  .nav-links a {
    display: block;
    padding: 0.45rem 0.9rem;
    color: var(--slate-light);
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border-radius: 6px;
    transition: color 0.2s, background 0.2s;
  }

  .nav-links a:hover,
  .nav-links a.active {
    color: var(--white);
    background: rgba(201,168,76,0.18);
  }

  .nav-links a.active {
    color: var(--gold);
  }

  /* hamburger */
  .hamburger {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
    padding: 4px;
  }
  .hamburger span {
    display: block;
    width: 24px; height: 2px;
    background: var(--gold);
    border-radius: 2px;
    transition: all 0.3s;
  }

  /* ── PAGES ── */
  .page {
    display: none;
    min-height: 100vh;
    padding-top: 64px;
    animation: fadeIn 0.4s ease;
  }
  .page.active { display: block; }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(12px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── HOME / HERO ── */
  #home {
    background: linear-gradient(135deg, var(--teal) 0%, var(--teal-mid) 55%, #0B4D5E 100%);
    min-height: 100vh;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
  }

  /* chalk-texture overlay */
  #home::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image:
      repeating-linear-gradient(0deg, transparent, transparent 31px, rgba(255,255,255,0.025) 32px),
      repeating-linear-gradient(90deg, transparent, transparent 31px, rgba(255,255,255,0.015) 32px);
    pointer-events: none;
  }

  .hero-inner {
    max-width: 1100px;
    margin: 0 auto;
    padding: 4rem 2rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5rem;
    align-items: center;
    position: relative;
    z-index: 1;
  }

  .hero-text .eyebrow {
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
  }

  .hero-text h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 5vw, 4.2rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.08;
    margin-bottom: 1.5rem;
  }

  .hero-text h1 .name-accent {
    color: var(--gold);
    display: block;
  }

  .hero-tagline {
    font-size: 1.05rem;
    color: var(--slate-light);
    line-height: 1.7;
    margin-bottom: 2.2rem;
    max-width: 420px;
  }

  .chalk-line {
    display: inline-block;
    position: relative;
  }
  .chalk-line::after {
    content: '';
    position: absolute;
    bottom: -4px; left:
