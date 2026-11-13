<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Makanan Populer Nasional — Katalog Kuliner Indonesia Modern</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --merah-utama: #DC2626;
      --merah-tua: #991B1B;
      --merah-lembut: #FEF2F2;
      --putih: #FFFFFF;
      --latar: #F8FAFC;
      --emas: #D97706;
      --emas-cerah: #F59E0B;
      --emas-lembut: #FFFBEB;
      --gelap: #0F172A;
      --teks-utama: #0F172A;
      --teks-sekunder: #334155;
      --border: #E2E8F0;
      --shadow-sm: 0 4px 12px rgba(15, 23, 42, 0.06);
      --shadow-md: 0 12px 30px rgba(15, 23, 42, 0.09);
      --shadow-red: 0 14px 32px rgba(220, 38, 38, 0.18);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
      background-color: var(--latar);
      color: var(--teks-utama);
      line-height: 1.65;
      overflow-x: hidden;
    }

    /* Pola Geometris Batik Kawung Halus */
    .batik-pattern {
      background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' stroke='%23DC2626' stroke-width='1' stroke-opacity='0.06'%3E%3Ccircle cx='30' cy='30' r='14'/%3E%3Ccircle cx='0' cy='0' r='14'/%3E%3Ccircle cx='60' cy='0' r='14'/%3E%3Ccircle cx='0' cy='60' r='14'/%3E%3Ccircle cx='60' cy='60' r='14'/%3E%3Cpath d='M30 16 L34 26 L44 30 L34 34 L30 44 L26 34 L16 30 L26 26 Z'/%3E%3C/g%3E%3C/svg%3E");
    }

    /* Sticky Navbar */
    .navbar {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: linear-gradient(90deg, var(--merah-utama) 0%, var(--merah-tua) 100%);
      color: var(--putih);
      padding: 0.9rem 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 20px rgba(153, 27, 27, 0.25);
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      text-decoration: none;
      color: var(--putih);
    }

    .brand-icon {
      width: 42px;
      height: 42px;
      background: var(--putih);
      color: var(--merah-utama);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      font-size: 1.25rem;
      border: 2px solid var(--emas-cerah);
      box-shadow: 0 4px 10px rgba(0,0,0,0.15);
    }

    .brand-text h1 {
      font-size: 1.15rem;
      font-weight: 800;
      letter-spacing: 0.8px;
      line-height: 1.2;
    }

    .brand-text span {
      font-size: 0.75rem;
      color: #FECACA;
      font-weight: 500;
      display: block;
    }

    .nav-links {
      display: flex;
      gap: 10px;
      list-style: none;
    }

    .nav-links a {
      color: var(--putih);
      text-decoration: none;
      font-size: 0.9rem;
      font-weight: 600;
      padding: 8px 16px;
      border-radius: 999px;
      transition: all 0.25s ease;
      border: 1px solid rgba(255,255,255,0.15);
    }

    .nav-links a:hover {
      background: var(--putih);
      color: var(--merah-utama);
      transform: translateY(-1px);
    }

    /* MENU 1: Hero & Profil Pembuat */
    .hero-section {
      padding: 70px 5% 80px;
      background: linear-gradient(135deg, #FFFFFF 0%, #FEF2F2 55%, #FFFBEB 100%);
      border-bottom: 1px solid var(--border);
      position: relative;
    }

    .hero-container {
      max-width: 1240px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 44px;
      align-items: center;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--merah-lembut);
      color: var(--merah-utama);
      border: 1px solid #FECACA;
      padding: 6px 16px;
      border-radius: 999px;
      font-size: 0.8rem;
      font-weight: 700;
      letter-spacing: 0.5px;
      margin-bottom: 18px;
    }

    .hero-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.3rem, 4.5vw, 3.6rem);
      font-weight: 800;
      color: var(--teks-utama);
      line-height: 1.15;
      margin-bottom: 18px;
    }

    .hero-title span {
      color: var(--merah-utama);
    }

    .hero-subtitle {
      font-size: 1.05rem;
      color: var(--teks-sekunder);
      margin-bottom: 30px;
      max-width: 600px;
    }

    .hero-stats {
      display: flex;
      gap: 24px;
      margin-bottom: 32px;
      flex-wrap: wrap;
    }

    .stat-item {
      background: var(--putih);
      padding: 12px 20px;
      border-radius: 14px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-sm);
    }

    .stat-item strong {
      display: block;
      font-size: 1.4rem;
      font-weight: 800;
      color: var(--merah-utama);
      line-height: 1.2;
    }

    .stat-item span {
      font-size: 0.8rem;
      color: var(--teks-sekunder);
      font-weight: 600;
    }

    .cta-btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: linear-gradient(135deg, var(--merah-utama) 0%, var(--merah-tua) 100%);
      color: var(--putih);
      text-decoration: none;
      font-weight: 700;
      font-size: 1rem;
      padding: 15px 30px;
      border-radius: 14px;
      box-shadow: var(--shadow-red);
      transition: all 0.3s ease;
    }

    .cta-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 18px 36px rgba(220, 38, 38, 0.28);
    }

    /* Kartu Profil Pembuat */
    .profile-card {
      background: var(--putih);
      border-radius: 22px;
      padding: 34px;
      box-shadow: var(--shadow-md);
      border: 1px solid var(--border);
      border-left: 8px solid var(--merah-utama);
      position: relative;
    }

    .profile-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 22px;
      padding-bottom: 14px;
      border-bottom: 2px dashed var(--border);
    }

    .profile-header h2 {
      font-size: 1.35rem;
      font-weight: 800;
      color: var(--merah-utama);
    }

    .profile-tag {
      background: var(--emas-lembut);
      color: var(--emas);
      border: 1px solid #FDE68A;
      font-size: 0.75rem;
      font-weight: 700;
      padding: 4px 12px;
      border-radius: 999px;
    }

    .profile-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
      margin-bottom: 20px;
    }

    .profile-field {
      background: var(--latar);
      padding: 12px 15px;
      border-radius: 12px;
      border: 1px solid var(--border);
    }

    .profile-field label {
      display: block;
      font-size: 0.72rem;
      text-transform: uppercase;
      letter-spacing: 0.6px;
      color: #64748B;
      font-weight: 700;
      margin-bottom: 2px;
    }

    .profile-field p {
      font-size: 0.98rem;
      font-weight: 700;
      color: var(--teks-utama);
    }

    .profile-reason {
      background: var(--merah-lembut);
      border: 1px solid #FECACA;
      padding: 16px 18px;
      border-radius: 14px;
    }

    .profile-reason label {
      display: block;
      font-size: 0.78rem;
      font-weight: 800;
      color: var(--merah-utama);
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 6px;
    }

    .profile-reason p {
      font-size: 0.92rem;
      color: var(--teks-sekunder);
      line-height: 1.6;
    }

    /* MENU 2: Katalog & Slide Interaktif */
    .catalog-section {
      padding: 75px 5%;
      max-width: 1280px;
      margin: 0 auto;
    }

    .section-header {
      text-align: center;
      margin-bottom: 36px;
    }

    .section-kicker {
      color: var(--emas);
      font-weight: 800;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      margin-bottom: 6px;
      display: block;
    }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.9rem, 3.5vw, 2.7rem);
      color: var(--merah-utama);
      font-weight: 800;
      margin-bottom: 10px;
    }

    .section-desc {
      color: var(--teks-sekunder);
      max-width: 680px;
      margin: 0 auto;
      font-size: 0.98rem;
    }

    /* Kontrol Pencarian, Filter & Pengalih Mode */
    .controls-panel {
      background: var(--putih);
      padding: 24px;
      border-radius: 20px;
      box-shadow: var(--shadow-sm);
      border: 1px solid var(--border);
      margin-bottom: 30px;
    }

    .search-row {
      display: flex;
      gap: 16px;
      align-items: center;
      flex-wrap: wrap;
      margin-bottom: 18px;
    }

    .search-box {
      flex: 1;
      min-width: 260px;
      position: relative;
      display: flex;
      align-items: center;
    }

    .search-box svg {
      position: absolute;
      left: 16px;
      color: var(--merah-utama);
      width: 20px;
      height: 20px;
    }

    .search-input {
      width: 100%;
      padding: 14px 44px 14px 46px;
      border: 2px solid #FCA5A5;
      border-radius: 14px;
      font-size: 0.96rem;
      font-family: inherit;
      color: var(--teks-utama);
      outline: none;
      transition: all 0.25s ease;
    }

    .search-input:focus {
      border-color: var(--merah-utama);
      box-shadow: 0 0 0 4px rgba(220, 38, 38, 0.12);
    }

    .clear-btn {
      position: absolute;
      right: 12px;
      background: #F1F5F9;
      border: none;
      color: #475569;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      cursor: pointer;
      font-weight: 700;
      display: none;
      align-items: center;
      justify-content: center;
    }

    .clear-btn:hover {
      background: var(--merah-utama);
      color: var(--putih);
    }

    .view-switcher {
      display: flex;
      background: #F1F5F9;
      padding: 5px;
      border-radius: 14px;
      gap: 4px;
    }

    .view-btn {
      border: none;
      background: transparent;
      padding: 10px 18px;
      border-radius: 10px;
      font-family: inherit;
      font-size: 0.88rem;
      font-weight: 700;
      color: #475569;
      cursor: pointer;
      transition: all 0.2s ease;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .view-btn.active {
      background: var(--merah-utama);
      color: var(--putih);
      box-shadow: 0 4px 10px rgba(220, 38, 38, 0.25);
    }

    .filter-tabs {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      padding-bottom: 14px;
      border-bottom: 1px solid var(--border);
      margin-bottom: 12px;
    }

    .filter-pill {
      border: 1px solid var(--border);
      background: var(--latar);
      color: var(--teks-sekunder);
      padding: 7px 15px;
      border-radius: 999px;
      font-family: inherit;
      font-size: 0.84rem;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .filter-pill:hover {
      border-color: var(--merah-utama);
      color: var(--merah-utama);
    }

    .filter-pill.active {
      background: var(--merah-utama);
      color: var(--putih);
      border-color: var(--merah-utama);
    }

    .result-info {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.86rem;
      color: #64748B;
      font-weight: 600;
      flex-wrap: wrap;
      gap: 8px;
    }

    /* MODE SLIDE PRESENTASI INTERAKTIF */
    .slide-stage {
      background: var(--putih);
      border-radius: 24px;
      box-shadow: var(--shadow-md);
      border: 1px solid var(--border);
      overflow: hidden;
      transition: all 0.3s ease;
    }

    .slide-card {
      display: grid;
      grid-template-columns: 0.95fr 1.05fr;
      min-height: 440px;
    }

    .slide-visual {
      background: linear-gradient(145deg, #FEF2F2 0%, #FFFBEB 100%);
      padding: 32px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      border-right: 1px solid var(--border);
      position: relative;
    }

    .slide-visual img {
      width: 100%;
      max-width: 390px;
      height: 280px;
      object-fit: cover;
      border-radius: 18px;
      box-shadow: 0 12px 28px rgba(15, 23, 42, 0.14);
      border: 4px solid var(--putih);
    }

    .slide-content {
      padding: 36px 40px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .slide-meta {
      display: flex;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 12px;
    }

    .num-badge {
      background: var(--merah-utama);
      color: var(--putih);
      font-weight: 800;
      font-size: 0.8rem;
      padding: 4px 12px;
      border-radius: 8px;
    }

    .origin-badge {
      background: var(--emas-lembut);
      color: var(--emas);
      border: 1px solid #FDE68A;
      font-weight: 700;
      font-size: 0.82rem;
      padding: 4px 14px;
      border-radius: 999px;
    }

    .slide-food-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.8rem, 3vw, 2.4rem);
      color: var(--merah-utama);
      font-weight: 800;
      margin-bottom: 18px;
      line-height: 1.2;
    }

    .info-block {
      background: var(--latar);
      border-left: 4px solid var(--emas-cerah);
      padding: 14px 18px;
      border-radius: 0 12px 12px 0;
      margin-bottom: 14px;
    }

    .info-block.sejarah {
      border-left-color: var(--merah-utama);
      background: #FFFDFD;
    }

    .info-block h4 {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.7px;
      color: var(--teks-utama);
      font-weight: 800;
      margin-bottom: 4px;
    }

    .info-block p {
      font-size: 0.95rem;
      color: var(--teks-sekunder);
    }

    .slide-controls {
      background: #F8FAFC;
      border-top: 1px solid var(--border);
      padding: 18px 32px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 16px;
      flex-wrap: wrap;
    }

    .nav-slide-btn {
      background: var(--putih);
      border: 2px solid var(--merah-utama);
      color: var(--merah-utama);
      font-family: inherit;
      font-weight: 700;
      font-size: 0.92rem;
      padding: 10px 22px;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    .nav-slide-btn:hover:not(:disabled) {
      background: var(--merah-utama);
      color: var(--putih);
    }

    .nav-slide-btn:disabled {
      opacity: 0.4;
      cursor: not-allowed;
    }

    .slide-indicator {
      font-weight: 800;
      color: var(--teks-utama);
      font-size: 0.95rem;
      background: var(--putih);
      padding: 8px 20px;
      border-radius: 999px;
      border: 1px solid var(--border);
    }

    /* MODE KATALOG GRID */
    .catalog-grid {
      display: none;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 26px;
    }

    .catalog-grid.active {
      display: grid;
    }

    .food-card {
      background: var(--putih);
      border-radius: 18px;
      overflow: hidden;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-sm);
      transition: all 0.3s ease;
      display: flex;
      flex-direction: column;
      cursor: pointer;
    }

    .food-card:hover {
      transform: translateY(-6px);
      box-shadow: var(--shadow-md);
      border-color: #FCA5A5;
    }

    .food-card-img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-bottom: 1px solid var(--border);
    }

    .food-card-body {
      padding: 22px;
      display: flex;
      flex-direction: column;
      flex: 1;
    }

    .food-card-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 8px;
      margin-bottom: 8px;
    }

    .food-card-title {
      font-size: 1.25rem;
      font-weight: 800;
      color: var(--merah-utama);
      margin-bottom: 10px;
    }

    .food-card-text {
      font-size: 0.88rem;
      color: var(--teks-sekunder);
      margin-bottom: 10px;
    }

    .food-card-footer {
      margin-top: auto;
      padding-top: 12px;
      border-top: 1px dashed var(--border);
      font-size: 0.8rem;
      font-weight: 700;
      color: var(--merah-utama);
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .empty-state {
      text-align: center;
      padding: 60px 20px;
      background: var(--putih);
      border-radius: 20px;
      border: 1px dashed #CBD5E1;
      display: none;
    }

    /* MENU 3: Pelestarian & Highlight Terima Kasih */
    .closing-section {
      background: linear-gradient(165deg, #0F172A 0%, #1E1B4B 45%, #450A0A 100%);
      color: var(--putih);
      padding: 85px 5% 95px;
      position: relative;
    }

    .closing-container {
      max-width: 1180px;
      margin: 0 auto;
    }

    .closing-header {
      text-align: center;
      margin-bottom: 48px;
    }

    .closing-header span {
      color: var(--emas-cerah);
      font-weight: 800;
      font-size: 0.85rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
    }

    .closing-header h2 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.9rem, 3.5vw, 2.7rem);
      margin-top: 8px;
      color: var(--putih);
    }

    .pillars-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 22px;
      margin-bottom: 56px;
    }

    .pillar-card {
      background: rgba(255, 255, 255, 0.06);
      backdrop-filter: blur(8px);
      border: 1px solid rgba(255, 255, 255, 0.14);
      border-top: 4px solid var(--emas-cerah);
      border-radius: 18px;
      padding: 26px;
      transition: transform 0.3s ease;
    }

    .pillar-card:hover {
      transform: translateY(-5px);
      background: rgba(255, 255, 255, 0.1);
    }

    .pillar-num {
      display: inline-block;
      background: var(--merah-utama);
      color: var(--putih);
      font-weight: 800;
      font-size: 0.8rem;
      padding: 4px 12px;
      border-radius: 999px;
      margin-bottom: 12px;
    }

    .pillar-card h3 {
      font-size: 1.15rem;
      font-weight: 700;
      margin-bottom: 10px;
      color: #FEF3C7;
    }

    .pillar-card p {
      font-size: 0.92rem;
      color: #CBD5E1;
      line-height: 1.65;
    }

    .thanks-wrapper {
      text-align: center;
      max-width: 820px;
      margin: 0 auto;
    }

    .thanks-message {
      font-size: 1.12rem;
      color: #E2E8F0;
      margin-bottom: 34px;
      line-height: 1.75;
    }

    .highlight-banner {
      background: var(--putih);
      border: 4px solid var(--emas-cerah);
      outline: 4px solid var(--merah-utama);
      border-radius: 24px;
      padding: 36px 28px;
      box-shadow: 0 0 50px rgba(245, 158, 11, 0.35), 0 20px 40px rgba(0, 0, 0, 0.45);
      display: inline-block;
      width: 100%;
    }

    .highlight-banner h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.5rem, 6vw, 4.4rem);
      font-weight: 800;
      color: var(--merah-utama);
      letter-spacing: 4px;
      text-transform: uppercase;
      line-height: 1.1;
      margin-bottom: 12px;
    }

    .highlight-banner p {
      color: var(--teks-sekunder);
      font-weight: 700;
      font-size: 0.92rem;
    }

    @media (max-width: 900px) {
      .hero-container,
      .slide-card {
        grid-template-columns: 1fr;
      }
      .slide-visual {
        border-right: none;
        border-bottom: 1px solid var(--border);
      }
      .slide-content {
        padding: 26px 22px;
      }
    }

    @media (max-width: 640px) {
      .nav-links {
        display: none;
      }
      .profile-grid {
        grid-template-columns: 1fr;
      }
      .slide-controls {
        justify-content: center;
      }
    }
  </style>
</head>
<body class="batik-pattern">

  <!-- Navigasi Atas -->
  <nav class="navbar">
    <a href="#menu1" class="brand">
      <div class="brand-icon">ID</div>
      <div class="brand-text">
        <h1>NUSANTARA RASA</h1>
        <span>Katalog Makanan Populer Nasional</span>
      </div>
    </a>
    <ul class="nav-links">
      <li><a href="#menu1">1. Profil Pembuat</a></li>
      <li><a href="#menu2">2. Katalog Kuliner (178)</a></li>
      <li><a href="#menu3">3. Pelestarian & Penutup</a></li>
    </ul>
  </nav>

  <!-- MENU PERTAMA: PROFIL PEMBUAT & TUJUAN WEBSITE -->
  <section id="menu1" class="hero-section">
    <div class="hero-container">
      <div>
        <div class="hero-badge">PROYEK DESAIN WEB INFORMATIKA • INDONESIA MODERN</div>
        <h1 class="hero-title">Makanan Populer <span>Nasional</span></h1>
        <p class="hero-subtitle">
          Katalog digital interaktif warisan kuliner Indonesia dari Sabang sampai Merauke yang mendunia—mencakup visual hidangan, komposisi bahan utama, daerah asal, serta sejarah terciptanya.
        </p>
        <div class="hero-stats">
          <div class="stat-item">
            <strong>178</strong>
            <span>Kuliner Nusantara</span>
          </div>
          <div class="stat-item">
            <strong>38</strong>
            <span>Provinsi Terwakili</span>
          </div>
          <div class="stat-item">
            <strong>100%</strong>
            <span>Warisan Budaya</span>
          </div>
        </div>
        <a href="#menu2" class="cta-btn">Jelajahi 178 Katalog Kuliner &rarr;</a>
      </div>

      <div class="profile-card">
        <div class="profile-header">
          <h2>Informasi Pembuat Website</h2>
          <span class="profile-tag">Tugas Informatika</span>
        </div>
        <div class="profile-grid">
          <div class="profile-field">
            <label>A. Nama Pembuat Website</label>
            <p>M. Jatmiko</p>
          </div>
          <div class="profile-field">
            <label>B. Kelas</label>
            <p>E-4</p>
          </div>
          <div class="profile-field">
            <label>C. Mata Pelajaran</label>
            <p>Informatika</p>
          </div>
          <div class="profile-field">
            <label>D. Tanggal Pembuatan</label>
            <p>7 Nov 2026</p>
          </div>
        </div>
        <div class="profile-reason">
          <label>E. Alasan Pembuatan Website</label>
          <p>
            Website ini dibuat untuk memperkenalkan makanan tradisional dari Indonesia yang populer hingga ke luar negeri dalam bentuk katalog digital interaktif, mencakup gambar makanan, bahan-bahan utama, asal daerah, serta sejarah terciptanya agar generasi muda semakin mengenal dan bangga terhadap kekayaan kuliner Nusantara.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- MENU KEDUA: KATALOG & SLIDE INTERAKTIF 178 MAKANAN -->
  <section id="menu2" class="catalog-section">
    <div class="section-header">
      <span class="section-kicker">Eksplorasi Kuliner Nusantara</span>
      <h2 class="section-title">Katalog 178 Makanan Populer Nasional</h2>
      <p class="section-desc">
        Gunakan fitur pencarian atau filter wilayah untuk menemukan hidangan favorit Anda. Anda dapat menjelajah dalam <strong>Mode Slide Presentasi</strong> maupun <strong>Mode Katalog Grid</strong>.
      </p>
    </div>

    <div class="controls-panel">
      <div class="search-row">
        <div class="search-box">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2">
            <circle cx="11" cy="11" r="8"></circle>
            <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
          </svg>
          <input type="text" id="searchInput" class="search-input" placeholder="Cari nama makanan, daerah asal, atau bahan utama (contoh: Rendang, Papua, Sate)..." />
          <button id="clearSearch" class="clear-btn" title="Hapus pencarian">&times;</button>
        </div>

        <div class="view-switcher">
          <button id="btnSlideView" class="view-btn active">Mode Slide Presentasi</button>
          <button id="btnGridView" class="view-btn">Mode Katalog Grid</button>
        </div>
      </div>

      <div class="filter-tabs" id="regionTabs">
        <button class="filter-pill active" data-region="Semua">Semua Wilayah (178)</button>
        <button class="filter-pill" data-region="Sumatera">Sumatera</button>
        <button class="filter-pill" data-region="Jawa & Jakarta">Jawa &amp; Jakarta</button>
        <button class="filter-pill" data-region="Bali & Nusa Tenggara">Bali &amp; Nusa Tenggara</button>
        <button class="filter-pill" data-region="Kalimantan">Kalimantan</button>
        <button class="filter-pill" data-region="Sulawesi">Sulawesi</button>
        <button class="filter-pill" data-region="Maluku & Papua">Maluku &amp; Papua</button>
      </div>

      <div class="result-info">
        <span id="resultCount">Menampilkan 178 dari 178 kuliner Nusantara</span>
        <span>Tip: Gunakan tombol panah &larr; / &rarr; pada keyboard untuk berpindah slide</span>
      </div>
    </div>

    <!-- Container Mode Slide -->
    <div id="slideStage" class="slide-stage">
      <div id="slideContentArea"></div>
      <div class="slide-controls">
        <button id="prevSlideBtn" class="nav-slide-btn">&larr; Slide Sebelumnya</button>
        <div id="slideIndicator" class="slide-indicator">Slide 1 dari 178</div>
        <button id="nextSlideBtn" class="nav-slide-btn">Slide Selanjutnya &rarr;</button>
      </div>
    </div>

    <!-- Container Mode Grid -->
    <div id="catalogGrid" class="catalog-grid"></div>

    <!-- State Kosong Jika Pencarian Tidak Ditemukan -->
    <div id="emptyState" class="empty-state">
      <h3 style="color: var(--merah-utama); margin-bottom: 8px;">Kuliner Tidak Ditemukan</h3>
      <p style="color: var(--teks-sekunder); margin-bottom: 16px;">Maaf, kata kunci yang Anda cari belum cocok dengan daftar 178 makanan.</p>
      <button onclick="resetFilter()" class="nav-slide-btn">Tampilkan Semua 178 Makanan</button>
    </div>
  </section>

  <!-- MENU KETIGA: PELESTARIAN & HIGHLIGHT TERIMA KASIH -->
  <section id="menu3" class="closing-section">
    <div class="closing-container">
      <div class="closing-header">
        <span>Warisan Budaya Takbenda</span>
        <h2>Mengapa Kita Harus Tetap Menjaga &amp; Melestarikan Makanan Nusantara?</h2>
      </div>

      <div class="pillars-grid">
        <div class="pillar-card">
          <span class="pillar-num">Pilar 01</span>
          <h3>Identitas &amp; Jati Diri Bangsa</h3>
          <p>Makanan tradisional adalah cerminan sejarah panjang, filosofi hidup, dan kearifan lokal setiap suku di Indonesia dari Sabang sampai Merauke.</p>
        </div>
        <div class="pillar-card">
          <span class="pillar-num">Pilar 02</span>
          <h3>Mencegah Kepunahan &amp; Klaim Budaya</h3>
          <p>Banyak kuliner Nusantara menggunakan teknik dan rempah langka yang wajib diwariskan kepada generasi muda agar tidak punah tergerus makanan cepat saji maupun diklaim pihak lain.</p>
        </div>
        <div class="pillar-card">
          <span class="pillar-num">Pilar 03</span>
          <h3>Penggerak Ekonomi Lokal &amp; UMKM</h3>
          <p>Melestarikan kuliner daerah berarti mendukung petani rempah, nelayan, peternak, serta jutaan pelaku usaha kuliner lokal di seluruh pelosok Indonesia.</p>
        </div>
        <div class="pillar-card">
          <span class="pillar-num">Pilar 04</span>
          <h3>Diplomasi Kuliner di Mata Dunia</h3>
          <p>Kekayaan rasa Nusantara adalah aset soft-power paling efektif untuk memperkenalkan keramahan dan pesona budaya Indonesia ke kancah internasional.</p>
        </div>
      </div>

      <div class="thanks-wrapper">
        <p class="thanks-message">
          Terima kasih telah berkunjung dan meluangkan waktu untuk menjelajahi 178 kekayaan rasa Nusantara di website <strong>Makanan Populer Nasional</strong> ini. Mari terus mencintai, bangga, dan melestarikan warisan kuliner Indonesia!
        </p>

        <div class="highlight-banner">
          <h1>TERIMA KASIH</h1>
          <p>Karya M. Jatmiko &bull; Kelas E-4 &bull; Mata Pelajaran Informatika &bull; 7 November 2026</p>
        </div>
      </div>
    </div>
  </section>

  <script>
    // Database Lengkap 178 Makanan Populer Nasional
    const makananData = [
      { id: 1, nama: "Rendang", asal: "Sumatera Barat", wilayah: "Sumatera", tipe: "daging", bahan: "Daging sapi, santan kelapa kental, cabai merah, lengkuas, serai, bawang merah, bawang putih, kunyit, dan rempah Minang.", sejarah: "Tercipta sebagai bekal perjalanan jauh masyarakat Minangkabau yang merantau; proses memasak berjam-jam hingga santan mengering membuat rendang awet berbulan-bulan." },
      { id: 2, nama: "Nasi Goreng", asal: "Jawa & Nasional", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Nasi putih, kecap manis, bawang merah, bawang putih, cabai, terasi, telur ayam, suwiran ayam, dan kerupuk.", sejarah: "Terinspirasi dari tradisi Tionghoa yang tidak membuang nasi sisa semalam, lalu diadaptasi masyarakat Nusantara dengan kecap manis hingga mendunia." },
      { id: 3, nama: "Sate Madura", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "sate", bahan: "Daging ayam atau kambing, kacang tanah sangrai giling, kecap manis, bawang merah, bawang putih, kemiri, dan jeruk limau.", sejarah: "Dipopulerkan perantau Madura sejak abad ke-19 dengan ciri khas potongan daging ramping dan siraman saus kacang kental berpadu kecap manis." },
      { id: 4, nama: "Sate Padang", asal: "Sumatera Barat", wilayah: "Sumatera", tipe: "sate", bahan: "Daging, lidah, atau jeroan sapi, tepung beras, kunyit, jahe, lengkuas, serai, jintan, ketumbar, dan ketupat.", sejarah: "Berasal dari Padang Panjang sejak era Kerajaan Pagaruyung sebagai hidangan upacara adat yang memanfaatkan kaldu daging menjadi saus rempah kental." },
      { id: 5, nama: "Sate Lilit", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "sate", bahan: "Daging ikan laut, ayam, atau babi cincang, parutan kelapa muda, santan, base genep Bali, dan batang serai.", sejarah: "Lahir dari tradisi upacara adat Bali; daging cincang dililitkan pada batang serai sebagai simbol persatuan dan kebersamaan masyarakat Bali." },
      { id: 6, nama: "Sate Maranggi", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "sate", bahan: "Daging sapi has dalam atau kambing, kecap manis, gula aren, ketumbar sangrai, lengkuas, jahe, asam jawa, dan sambal tomat.", sejarah: "Berkembang di Purwakarta dan Cianjur; daging dimarinasi rempah sebelum dibakar sehingga tidak perlu saus kacang, konon dinamai dari penjual legendaris Mak Ranggi." },
      { id: 7, nama: "Soto Lamongan", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Ayam kampung suwir, kuah kaldu kuning kunyit, serai, daun jeruk, soun, kol, telur rebus, dan bubuk koya udang.", sejarah: "Diciptakan perantau asal Lamongan yang memadukan soto berkuah kuning dengan inovasi taburan bubuk koya gurih." },
      { id: 8, nama: "Soto Betawi", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging dan jeroan sapi, santan dan susu sapi segar, serai, daun salam, kayu manis, cengkeh, kentang goreng, dan emping.", sejarah: "Dipopulerkan pedagang kuliner Betawi pada pertengahan abad ke-20 yang memadukan rempah Nusantara dengan susu dan santan pengaruh Belanda dan Arab." },
      { id: 9, nama: "Soto Banjar", asal: "Kalimantan Selatan", wilayah: "Kalimantan", tipe: "kuah", bahan: "Daging ayam kampung, kayu manis, cengkeh, kapulaga, bunga lawang, susu evaporasi, ketupat, perkedel kentang, dan telur rebus.", sejarah: "Tercipta dari akulturasi budaya Melayu Banjar, Tionghoa, dan Timur Tengah di Banjarmasin dengan aroma rempah wangi yang khas." },
      { id: 10, nama: "Coto Makassar", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kuah", bahan: "Daging dan jeroan sapi, kacang tanah sangrai giling halus, air cucian beras (tajin), serai, lengkuas, ketumbar, jintan, dan buras.", sejarah: "Sudah ada sejak era Kerajaan Gowa abad ke-16 sebagai hidangan penambah tenaga bagi prajurit istana dengan memanfaatkan air tajin dan kacang." },
      { id: 11, nama: "Gado-gado", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Sayuran rebus (kangkung, bayam, tauge, kacang panjang), lontong, tahu, tempe, telur rebus, kerupuk, dan saus kacang ulek.", sejarah: "Lahir dari interaksi budaya Betawi, Tionghoa, dan Eropa di Batavia abad ke-17; dijuluki dunia sebagai Indonesian Salad." },
      { id: 12, nama: "Pecel", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Sayuran rebus (bayam, tauge, kacang panjang, kembang turi), sambal kacang kencur daun jeruk, rempeyek kacang, dan nasi hangat.", sejarah: "Tercatat dalam Serat Centhini dan babad kuno; kata pecel bermakna diperas, merujuk pada sayuran rebus yang diperas sebelum disiram sambal kacang." },
      { id: 13, nama: "Ketoprak", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Ketupat, tahu putih goreng, bihun seduh, tauge segar, mentimun, kerupuk, bawang putih mentah, cabai rawit, kacang goreng, dan kecap manis.", sejarah: "Berkembang di kalangan masyarakat Betawi dan pedagang Cirebon di Jakarta; namanya konon berasal dari bunyi piring jatuh ketuprakk." },
      { id: 14, nama: "Bakso", asal: "Jawa Tengah & Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging sapi giling halus, tepung tapioka, bawang putih, merica, kaldu tulang sapi bening, mie kuning, bihun, dan sawi hijau.", sejarah: "Berasal dari akulturasi kuliner Tionghoa-Jawa (Bak-So berarti daging giling) yang diadaptasi menggunakan daging sapi halal di Wonogiri dan Malang." },
      { id: 15, nama: "Mie Ayam", asal: "Jawa & Nasional", wilayah: "Jawa & Jakarta", tipe: "mie", bahan: "Mie telur kenyal, potongan daging ayam kecap manis gurih, minyak bawang ayam, sawi hijau, daun bawang, pangsit, dan kuah kaldu.", sejarah: "Adaptasi hidangan mie tradisi Tionghoa selatan yang disesuaikan oleh masyarakat Wonogiri dengan bumbu tumisan ayam kecap manis gurih." },
      { id: 16, nama: "Gudeg", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Nangka muda (gori), santan kelapa, gula aren, daun jati (memberi warna cokelat kemerahan), telur pindang, ayam kampung, dan krecek.", sejarah: "Tercipta pada abad ke-16 saat prajurit Mataram Islam membuka hutan Mentaok dan memasak melimpahnya buah nangka muda dalam kuali besar." },
      { id: 17, nama: "Pempek", asal: "Sumatera Selatan", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan tenggiri giling, tepung sagu/tapioka, telur, air es, serta kuah cuko dari gula aren batok, asam jawa, bawang putih, dan cabai rawit.", sejarah: "Lahir pada masa Kesultanan Palembang abad ke-16 ketika perantau Tionghoa (Apek) mengolah limpahan ikan Sungai Musi bersama sagu." },
      { id: 18, nama: "Rawon", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging sapi sandung lamur, keluak (kluwek) sebagai pewarna hitam alami, serai, daun jeruk, lengkuas, tauge pendek, dan telur asin.", sejarah: "Tercatat dalam Prasasti Taji (901 M) era Kerajaan Mataram Kuno bernama Rarawwan, menggunakan kluwek sebagai bumbu penyedap alami." },
      { id: 19, nama: "Ayam Betutu", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "daging", bahan: "Ayam kampung utuh, base genep lengkap (kunyit, lengkuas, jahe, kencur, serai, cabai, terasi), daun singkong, dan daun pisang.", sejarah: "Berasal dari Gianyar dan Gilimanuk sejak era Majapahit di Bali; ayam dipanggang dalam sekam panas berjam-jam untuk upacara adat." },
      { id: 20, nama: "Papeda", asal: "Papua & Maluku", wilayah: "Maluku & Papua", tipe: "nasi", bahan: "Tepung sari pati pohon sagu murni, air panas mendidih, dan perasan jeruk nipis; disajikan bersama ikan kuah kuning.", sejarah: "Pangan pokok purba masyarakat adat Papua dan Maluku yang hidup berdampingan dengan hutan sagu sebagai pohon kehidupan." },
      { id: 21, nama: "Nasi Uduk", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Beras putih dikukus dengan santan, daun salam, serai, lengkuas, cengkeh, ayam goreng, semur tahu, bihun, dan bawang goreng.", sejarah: "Dikenal sejak era Kesultanan Mataram dan berkembang di Batavia; kata uduk bermakna bercampur, mencerminkan nasi gurih dengan beragam lauk." },
      { id: 22, nama: "Nasi Kuning", asal: "Jawa & Nasional", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Beras putih, santan kelapa, kunyit segar, serai, daun salam, daun pandan, ayam goreng, telur dadar iris, dan kering tempe.", sejarah: "Warna kuning melambangkan emas dan kemakmuran dalam budaya Nusantara sehingga selalu hadir pada acara syukuran dan peresmian." },
      { id: 23, nama: "Nasi Padang", asal: "Sumatera Barat", wilayah: "Sumatera", tipe: "nasi", bahan: "Nasi putih hangat dengan rendang, gulai ayam, gulai nangka (cubadak), daun singkong rebus, dan sambal lado hijau.", sejarah: "Berkembang dari tradisi Lapau Minang dan menyebar ke seluruh Indonesia seiring budaya merantau masyarakat Minangkabau." },
      { id: 24, nama: "Ayam Pop", asal: "Sumatera Barat", wilayah: "Sumatera", tipe: "daging", bahan: "Ayam kampung muda tanpa kulit, air kelapa muda, bawang putih, jahe, serai, daun salam, dan sambal tomat merah halus.", sejarah: "Dipopulerkan di Bukittinggi tahun 1960-an; ayam direbus dalam air kelapa berbumbu lalu digoreng sekejap agar tetap putih lembut." },
      { id: 25, nama: "Dendeng Balado", asal: "Sumatera Barat", wilayah: "Sumatera", tipe: "daging", bahan: "Daging sapi has dalam iris tipis lebar, bawang putih, ketumbar, air asam, dan sambal cabai merah tumbuk kasar.", sejarah: "Lahir dari kebutuhan masyarakat Minang mengawetkan daging sapi melalui pengeringan renyah berpadu sambal cabai segar." },
      { id: 26, nama: "Gulai Tunjang", asal: "Sumatera Barat", wilayah: "Sumatera", tipe: "kuah", bahan: "Tunjang (kikil/kaki sapi empuk), santan kelapa, cabai merah, kunyit, lengkuas, serai, daun kunyit, dan asam kandis.", sejarah: "Mencerminkan filosofi masyarakat Minangkabau yang menghargai bahan pangan dengan mengolah kaki sapi menjadi hidangan kaya rempah." },
      { id: 27, nama: "Opor Ayam", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging ayam kampung, santan kelapa, kemiri sangrai, ketumbar, jintan, bawang merah, bawang putih, lengkuas, dan serai.", sejarah: "Tercipta dari akulturasi kuliner Jawa dengan kari India pada masa penyebaran Islam; identik sebagai hidangan wajib Idulfitri." },
      { id: 28, nama: "Sayur Asem", asal: "Jawa Barat & Betawi", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Melinjo, daun melinjo, kacang tanah, jagung manis, labu siam, kacang panjang, asam jawa muda, terasi, dan cabai merah.", sejarah: "Lahir dari kearifan masyarakat agraris Sunda dan Betawi memanfaatkan hasil kebun pekarangan dengan kuah segar asam manis." },
      { id: 29, nama: "Sayur Lodeh", asal: "Jawa", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Labu siam, terong ungu, kacang panjang, tempe semangit, melinjo, santan encer, bawang merah, kemiri, dan daun salam.", sejarah: "Dipercaya dalam tradisi masyarakat Yogyakarta sebagai hidangan tolak bala sejak abad ke-16 saat memohon keselamatan dari wabah." },
      { id: 30, nama: "Pepes Ikan", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "ikan", bahan: "Ikan mas, nila, atau kembung segar, kunyit, kemiri, bawang merah, serai, daun kemangi, cabai rawit, dan pembungkus daun pisang.", sejarah: "Berasal dari bahasa Sunda pais, teknik kuno membungkus bahan makanan dengan daun pisang lalu dikukus dan dibakar di atas bara." },
      { id: 31, nama: "Ikan Bakar Jimbaran", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "ikan", bahan: "Ikan laut segar (kakap, baronang, kerapu), bumbu bawang putih, cabai merah, terasi Bali, air jeruk limau, dan sambal matah.", sejarah: "Bermula dari perkampungan nelayan tradisional Pantai Jimbaran yang membakar ikan menggunakan sabut kelapa kering." },
      { id: 32, nama: "Babi Guling", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "daging", bahan: "Babi muda utuh, base genep lengkap (kunyit, kencur, jahe, lengkuas, bawang putih, ketumbar, terasi), daun singkong, dan santan.", sejarah: "Hidangan sakral dalam upacara keagamaan dan adat Bali yang dipanggang utuh sambil diputar (diguling) di atas bara api." },
      { id: 33, nama: "Lawar", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Sayuran cincang (nangka muda atau kacang panjang), kelapa parut sangrai, daging cincang, base genep, terasi bakar, dan jeruk limau.", sejarah: "Berasal dari tradisi gotong royong masyarakat Bali (ngayah) saat mempersiapkan upacara adat bersama-sama." },
      { id: 34, nama: "Martabak Manis", asal: "Bangka Belitung & Nasional", wilayah: "Sumatera", tipe: "kue", bahan: "Tepung terigu, telur, gula pasir, ragi/soda kue, mentega, susu kental manis, cokelat meses, kacang sangrai, dan keju.", sejarah: "Berasal dari Pulau Bangka bernama asli Hok Lo Pan pada abad ke-19, lalu berkembang menjadi jajanan malam legendaris." },
      { id: 35, nama: "Martabak Telur", asal: "Sumatera Selatan & Nasional", wilayah: "Sumatera", tipe: "kue", bahan: "Adonan kulit tepung terigu elastis, telur bebek/ayam, daging cincang berbumbu kari, daun bawang melimpah, dan kuah cuko/acar.", sejarah: "Lahir dari perpaduan budaya pedagang Muslim India (Mutabbaq) yang menikah dengan warga lokal di Palembang dan Tegal." },
      { id: 36, nama: "Siomay", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "ikan", bahan: "Ikan tenggiri giling, tepung tapioka, labu siam, tahu putih, kentang, kubis gulung, telur rebus, saus kacang kental, dan jeruk limau.", sejarah: "Adaptasi dim sum Shumai dari Tiongkok yang disesuaikan masyarakat Bandung menggunakan ikan tenggiri halal dan saus kacang." },
      { id: 37, nama: "Batagor", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "ikan", bahan: "Adonan ikan tenggiri dan tepung sagu diisikan ke tahu putih dan kulit pangsit lalu digoreng garing, disajikan dengan saus kacang.", sejarah: "Singkatan Bakso Tahu Goreng; tercipta di Bandung akhir 1960-an ketika Haji Isan menggoreng sisa bakso tahu yang tidak habis terjual." },
      { id: 38, nama: "Kerak Telor", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Beras ketan putih rendam, telur bebek atau ayam, ebi sangrai, serundeng kelapa sangrai manis gurih, bawang goreng, dan merica.", sejarah: "Diciptakan masyarakat Betawi era 1920-an dari melimpahnya buah kelapa di Jakarta, dimasak di atas tungku arang hingga berkerak harum." },
      { id: 39, nama: "Seblak", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "mie", bahan: "Kerupuk aci mentah direndam kenyal, kencur (cikur), bawang putih, cabai rawit, telur orak-arik, bakso, sosis, dan ceker ayam.", sejarah: "Populer di Bandung sejak awal 2000-an sebagai inovasi mengolah kerupuk aci dengan kuah pedas beraroma kuat kencur." },
      { id: 40, nama: "Bakpia", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Kulit pastry tipis berlapis dari tepung terigu dan minyak, dengan isian kacang hijau kupas halus manis gurih.", sejarah: "Terinspirasi kue Tou Luk Pia yang dibawa perantau Tionghoa ke kawasan Pathok Yogyakarta tahun 1948 dan diadaptasi halal." },
      { id: 41, nama: "Lumpia Semarang", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Kulit lumpia tipis renyah, rebung manis gurih, telur orak-arik, udang cincang, bawang putih, dan saus kental manis bawang.", sejarah: "Lahir abad ke-19 di Semarang dari perpaduan resep pasangan Tjoa Thay Joe dan Mbak Wasih yang mengganti isian dengan rebung dan udang." },
      { id: 42, nama: "Serabi", asal: "Jawa Barat & Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Tepung beras, santan kelapa kental, parutan kelapa, sedikit ragi, dan gula aren cair (kinca) atau topping modern.", sejarah: "Sudah dikenal sejak era Mataram Kuno dan tercatat dalam Serat Centhini; dipanggang di atas cetakan tanah liat berbahan bakar kayu." },
      { id: 43, nama: "Klepon", asal: "Jawa", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Tepung ketan putih, sari daun pandan dan daun suji hijau alami, isian gula merah sisir, dan taburan kelapa parut kukus.", sejarah: "Kue tradisional Jawa sejak abad ke-15; bentuk bulat hijau berisi gula merah cair melambangkan kesederhanaan yang menyimpan kebaikan." },
      { id: 44, nama: "Onde-onde", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Tepung ketan, sedikit tepung beras, wijen putih melimpah di luar, dan isian pasta kacang hijau kupas manis di dalam.", sejarah: "Dibawa Laksamana Cheng Ho ke wilayah Majapahit (Mojokerto) abad ke-14, lalu diadaptasi dengan isian kacang hijau manis." },
      { id: 45, nama: "Lemper", asal: "Jawa", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Beras ketan putih kukus santan daun pandan, isian abon ayam atau daging ayam suwir berbumbu gurih, serta pembungkus daun pisang.", sejarah: "Kudapan tradisional Jawa dalam acara selamatan; tekstur ketan yang lengket melambangkan eratnya tali persaudaraan." },
      { id: 46, nama: "Mie Aceh", asal: "Aceh", wilayah: "Sumatera", tipe: "mie", bahan: "Mie kuning tebal kenyal, irisan daging sapi/kambing atau seafood, kapulaga, jintan, adas, cabai kering, tomat, dan acar bawang.", sejarah: "Mencerminkan posisi Aceh sebagai bandar internasional; memadukan mie Tionghoa dengan kuah kari kaya rempah India dan Timur Tengah." },
      { id: 47, nama: "Ayam Tangkap", asal: "Aceh", wilayah: "Sumatera", tipe: "daging", bahan: "Ayam kampung potong kecil, daun temurui (daun kari), daun pandan iris, cabai hijau keriting, serai, bawang putih, dan kunyit.", sejarah: "Berasal dari Aceh Besar; ayam digoreng bersama limpahan rempah daun hijau hingga garing sehingga ayam tampak tertangkap dedaunan." },
      { id: 48, nama: "Kuah Pliek U", asal: "Aceh", wilayah: "Sumatera", tipe: "sayur", bahan: "Pliek u (ampas kelapa fermentasi khas Aceh), daun melinjo, buah melinjo, nangka muda, kacang panjang, daun kari, dan serai.", sejarah: "Hidangan pemersatu masyarakat Aceh yang melambangkan kekayaan hasil bumi Tanah Rencong menggunakan pliek u fermentasi." },
      { id: 49, nama: "Sie Reuboh", asal: "Aceh", wilayah: "Sumatera", tipe: "daging", bahan: "Daging sapi atau kerbau berlemak, cuka aren (ie jok) khas Aceh, cabai merah kering, cabai rawit, bawang putih, dan kunyit.", sejarah: "Diciptakan sebagai makanan awet bagi para pejuang Aceh; daging direbus dengan cuka aren dalam belanga tanah liat agar tahan berminggu-minggu." },
      { id: 50, nama: "Arsik", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan mas segar bersisik, andaliman (merica Batak), asam cikala (kecombrang), bawang batak (lokio), kunyit, dan kacang panjang.", sejarah: "Hidangan sakral adat Batak Toba yang melambangkan doa berkat dan kemurnian hidup pada upacara kelahiran hingga pernikahan." },
      { id: 51, nama: "Saksang", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "daging", bahan: "Daging cincang tradisional, andaliman, kelapa parut sangrai, serai, lengkuas, kunyit, dan rempah khas Batak.", sejarah: "Kuliner wajib dalam pesta adat dan pernikahan masyarakat Batak Toba yang melambangkan kebersamaan dan penghormatan tamu." },
      { id: 52, nama: "Bika Ambon", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "kue", bahan: "Tepung tapioka, kuning telur ayam melimpah, santan kental, gula pasir, air nira (tuak enau) pengembang alami, dan daun jeruk.", sejarah: "Diciptakan di Jalan Ambon Medan melalui eksperimen memodifikasi kue bingka Melayu dengan fermentasi nira hingga bersarang." },
      { id: 53, nama: "Soto Medan", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "kuah", bahan: "Daging ayam atau sapi, santan kental, serai, daun jeruk, bunga lawang, kapulaga, jintan, kentang goreng, dan perkedel.", sejarah: "Berkembang di Medan sebagai titik temu budaya Melayu Deli, India, dan Tionghoa dengan kuah santan kuning gurih berempah." },
      { id: 54, nama: "Mie Gomak", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "mie", bahan: "Mie lidi besar (Spageti Batak), andaliman, santan kelapa atau bumbu goreng, labu siam, bawang merah, dan cabai.", sejarah: "Berasal dari kawasan Danau Toba; dinamai gomak karena dahulu pedagang mengambil dan menata mie langsung menggunakan tangan." },
      { id: 55, nama: "Gulai Ikan Patin", asal: "Jambi & Riau", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan patin sungai segar, santan kelapa, kunyit, lengkuas, serai, asam kandis, cabai merah, dan daun kunyit.", sejarah: "Berakar dari tradisi Melayu di sepanjang Sungai Batanghari dan Siak yang mengolah ikan patin segar dengan rempah kuning." },
      { id: 56, nama: "Tempoyak", asal: "Jambi & Sumatera Selatan", wilayah: "Sumatera", tipe: "ikan", bahan: "Daging buah durian matang fermentasi, cabai merah giling, kunyit, serai, dan ikan patin atau udang.", sejarah: "Tercipta dari kearifan lokal masyarakat Melayu Sumatera saat panen durian melimpah untuk mengawetkan durian menjadi bumbu." },
      { id: 57, nama: "Pendap", asal: "Bengkulu", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan laut (kakap/kembung), kelapa parut muda, bawang putih, lengkuas, cabai merah, asam kandis, dan daun talas berlapis.", sejarah: "Kuliner legendaris Bengkulu sejak era kolonial dan pengasingan Bung Karno; dikukus 8 jam hingga daun talasnya empuk nikmat." },
      { id: 58, nama: "Bagar Hiu", asal: "Bengkulu", wilayah: "Sumatera", tipe: "ikan", bahan: "Daging ikan hiu punai/tanduk, kelapa parut sangrai halus, ketumbar, jintan, cengkeh, kapulaga, kayu manis, dan asam jawa.", sejarah: "Hidangan langka pesisir Bengkulu tanpa santan melainkan kelapa sangrai pekat; dikenal sebagai hidangan favorit Bung Karno." },
      { id: 59, nama: "Tekwan", asal: "Sumatera Selatan", wilayah: "Sumatera", tipe: "kuah", bahan: "Adonan ikan tenggiri giling dan sagu berbentuk bulatan kecil, kaldu kepala udang bening, jamur kuping, bengkuang, dan soun.", sejarah: "Terinspirasi sup bakso ikan Tionghoa di Palembang berpadu kaldu udang lokal; namanya dari frasa berkotek samo kawan." },
      { id: 60, nama: "Model", asal: "Sumatera Selatan", wilayah: "Sumatera", tipe: "kuah", bahan: "Adonan pempek ikan tenggiri membungkus tahu putih lalu digoreng, disajikan dengan kuah kaldu udang bening, mentimun, dan soun.", sejarah: "Variasi kreatif keluarga pempek Palembang yang memadukan adonan ikan kenyal, tahu goreng lembut, dan kaldu udang." },
      { id: 61, nama: "Pindang Patin", asal: "Sumatera Selatan", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan patin segar, nanas potong, serai, lengkuas, asam jawa, cabai merah, tomat, terasi, kecap manis, dan daun kemangi.", sejarah: "Lahir dari budaya masyarakat tepian Sungai Musi yang mengolah ikan sungai segar dengan kuah asam pedas manis tanpa santan." },
      { id: 62, nama: "Mie Celor", asal: "Sumatera Selatan", wilayah: "Sumatera", tipe: "mie", bahan: "Mie telur ukuran besar, kaldu ebi kental bersantan, tauge, telur rebus iris, daun kucai, dan bawang goreng.", sejarah: "Kata celor bermakna diseduh air panas dalam bahasa Palembang; hasil akulturasi kuliner Tionghoa dan Melayu Palembang." },
      { id: 63, nama: "Lempah Kuning", asal: "Bangka Belitung", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan kakap merah atau tenggiri segar, kunyit, lengkuas, terasi khas Bangka, cabai merah, asam jawa, dan potongan nanas.", sejarah: "Warisan bahari masyarakat Bangka Belitung yang memadukan hasil tangkapan laut segar dengan bumbu kuning dan nanas lokal." },
      { id: 64, nama: "Otak-otak", asal: "Kepulauan Riau & Sumsel", wilayah: "Sumatera", tipe: "ikan", bahan: "Daging ikan tenggiri giling halus, santan kelapa, tepung sagu, bawang merah, bawang putih, daun bawang, dan daun pisang/kelapa.", sejarah: "Berkembang di pesisir Selat Malaka dan Bangka; dinamai otak-otak karena teksturnya yang putih lembut saat dibuka dari panggangan." },
      { id: 65, nama: "Mie Tarempa", asal: "Kepulauan Riau", wilayah: "Sumatera", tipe: "mie", bahan: "Mie kuning pipih kenyal, suwiran ikan tongkol segar, tauge, telur, kecap asin, kecap manis, cabai merah, dan acar cabai rawit.", sejarah: "Berasal dari Kota Tarempa di Kepulauan Anambas; akulturasi warga Melayu dan Tionghoa memanfaatkan ikan tongkol laut Natuna." },
      { id: 66, nama: "Lakse", asal: "Kepulauan Riau", wilayah: "Sumatera", tipe: "mie", bahan: "Mie sagu putih kenyal, kuah santan ikan tongkol giling, ketumbar, jintan, adas, kunyit, bawang merah, dan sambal belacan.", sejarah: "Kuliner tradisional Melayu Lingga dan Bintan yang memanfaatkan sagu sebagai mie utama berpadu kuah gulai ikan tongkol." },
      { id: 67, nama: "Gonggong", asal: "Kepulauan Riau", wilayah: "Sumatera", tipe: "ikan", bahan: "Siput laut gonggong khas perairan Bintan dan Batam direbus dengan serai, jahe, dan garam, disajikan dengan sambal kacang asam.", sejarah: "Siput laut endemik perairan Kepulauan Riau yang menjadi sumber protein masyarakat pesisir Melayu sejak ratusan tahun lalu." },
      { id: 68, nama: "Seruit", asal: "Lampung", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan sungai bakar atau goreng (baung/belida), sambal terasi bakar, tempoyak atau mangga kuini muda, dan lalapan segar.", sejarah: "Berasal dari kata nyeruit (dilakukan bersama-sama); tradisi makan komunal masyarakat adat Lampung untuk mempererat silaturahmi." },
      { id: 69, nama: "Nasi Tutug Oncom", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Nasi putih hangat ditumbuk bersama oncom bakar berbumbu kencur, bawang merah, cabai rawit, terasi, ayam goreng, dan lalapan.", sejarah: "Berasal dari Tasikmalaya tahun 1940-an; kreativitas masyarakat Sunda mengolah oncom menjadi lauk ekonomis yang sangat gurih." },
      { id: 70, nama: "Karedok", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Sayuran mentah segar (kacang panjang, kol, tauge, mentimun, terong bulat hijau, kemangi), kacang tanah, kencur, terasi, dan gula aren.", sejarah: "Kuliner khas Sunda sejak era Kerajaan Pajajaran; seluruh sayuran disajikan mentah segar dengan aroma kencur yang kuat." },
      { id: 71, nama: "Empal Gentong", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging sapi, usus, babat, santan kelapa, kunyit, kapulaga, cengkeh, kayu manis, serai, kucai iris, dan bubuk cabai kering.", sejarah: "Berasal dari Cirebon sejak abad ke-15; dimasak di dalam periuk tanah liat (gentong) menggunakan kayu bakar pohon mangga." },
      { id: 72, nama: "Nasi Jamblang", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Nasi putih pulen dibungkus daun jati, sambal goreng cabai merah iris, semur tahu, sate kentang, paru goreng, dan balakutak.", sejarah: "Diciptakan Haji Abdul Latif di Desa Jamblang Cirebon abad ke-19; pembungkus daun jati menjaga nasi tetap pulen dan tahan lama." },
      { id: 73, nama: "Tahu Gejrot", asal: "Jawa Barat", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Tahu pong goreng khas Cirebon, kuah gula aren, asam jawa, kecap manis, serta ulekan kasar bawang merah, bawang putih, dan cabai rawit.", sejarah: "Berasal dari Ciledug Cirebon; dinamai gejrot dari bunyi kuah gula asam yang dituangkan dari botol ke atas piring tahu." },
      { id: 74, nama: "Kupat Tahu", asal: "Jawa Barat & Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Ketupat, tahu putih goreng setengah matang, tauge rebus, kol iris, kerupuk, dan siraman bumbu kacang manis gurih.", sejarah: "Hidangan rakyat di jalur perdagangan Priangan dan Jawa Tengah sebagai sarapan praktis memadukan ketupat, tahu, dan saus kacang." },
      { id: 75, nama: "Garang Asem", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "daging", bahan: "Daging ayam kampung potong, belimbing wuluh segar, tomat hijau, cabai rawit utuh, santan encer, lengkuas, dan daun pisang.", sejarah: "Berasal dari Grobogan dan Kudus; teknik mengukus ayam berkuah belimbing wuluh dalam daun pisang menghasilkan rasa asam segar." },
      { id: 76, nama: "Nasi Liwet Solo", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Beras dimasak dengan santan dan kaldu ayam, disajikan di atas pincuk daun pisang dengan sayur labu siam, suwiran ayam, dan areh.", sejarah: "Berasal dari Desa Menuran Sukoharjo abad ke-19 untuk dijual kepada pekerja dan abdi dalem Keraton Kasunanan Surakarta." },
      { id: 77, nama: "Selat Solo", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "daging", bahan: "Daging sapi has dalam masak semur manis gurih, kentang goreng, buncis rebus, wortel, selada, telur pindang, dan saus moster.", sejarah: "Tercipta di dapur Keraton Kasunanan Surakarta era kolonial sebagai akulturasi bistik/salad Eropa dengan selera manis Jawa." },
      { id: 78, nama: "Tengkleng", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Tulang-belulang kambing (iga, kepala, kaki), kuah gulai encer tanpa santan kental, kunyit, jahe, serai, cengkeh, dan cabai rawit.", sejarah: "Lahir pada masa penjajahan di Solo ketika rakyat biasa mengolah bagian tulang dan kepala kambing menjadi gulai encer lezat." },
      { id: 79, nama: "Tongseng", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging kambing atau sapi potong, kuah gulai berempah, kol iris segar, tomat merah, cabai rawit, bawang merah, dan kecap manis.", sejarah: "Berkembang di Boyolali dan Solo abad ke-19 sebagai pengembangan gulai kambing yang ditumis ulang bersama sayuran dan kecap." },
      { id: 80, nama: "Nasi Gandul", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Nasi putih beralas daun pisang, potongan daging dan jeroan sapi berkuah cokelat gurih manis berempah kluwek, dan tempe goreng.", sejarah: "Berasal dari Desa Gajahmati Pati; dinamai gandul karena penjualnya memikul kuali dan bakul nasi yang bergantung pada pikulan bambu." },
      { id: 81, nama: "Soto Kudus", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging kerbau atau ayam suwir, kuah kaldu bening beraroma bawang putih goreng dan jintan, tauge rebus, seledri, dan jeruk nipis.", sejarah: "Berakar dari ajaran toleransi Sunan Kudus abad ke-16 yang menganjurkan mengganti daging sapi dengan daging kerbau." },
      { id: 82, nama: "Tahu Gimbal", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Tahu putih goreng, gimbal (bakwan udang goreng renyah), lontong, kol iris mentah, tauge, telur ceplok, dan saus kacang petis.", sejarah: "Kuliner ikonik Semarang yang memadukan tahu goreng dan bakwan udang bertumpuk-tumpuk (gimbal) dengan saus kacang petis." },
      { id: 83, nama: "Mangut Lele", asal: "DI Yogyakarta & Jateng", wilayah: "Jawa & Jakarta", tipe: "ikan", bahan: "Ikan lele asap atau goreng kering, kuah santan pedas kemerahan, kencur, cabai rawit, lengkuas, daun salam, dan kemangi.", sejarah: "Berasal dari tradisi masyarakat Bantul dan pesisir utara Jawa yang mengawetkan ikan lele dengan pengasapan sebelum dimasak santan." },
      { id: 84, nama: "Brongkos", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging sapi sandung lamur, kacang tolo, tahu kulit, telur rebus, kluwek pewarna cokelat gelap, santan, dan cabai rawit utuh.", sejarah: "Hidangan klasik kegemaran Sri Sultan Hamengkubuwono IX di Keraton Yogyakarta yang memadukan gurihnya santan, kluwek, dan kacang tolo." },
      { id: 85, nama: "Oseng Mercon", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "daging", bahan: "Tetelan dan kikil daging sapi empuk yang ditumis dengan cabai rawit merah melimpah, bawang merah, bawang putih, dan lengkuas.", sejarah: "Dipopulerkan Bu Narti di Yogyakarta tahun 1997 saat mengolah melimpahnya daging kurban dengan puluhan kilogram cabai rawit." },
      { id: 86, nama: "Tiwul", asal: "DI Yogyakarta & Jatim", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Tepung gaplek (singkong kupas yang dijemur kering lalu ditumbuk), air, gula merah sisir, dan taburan kelapa parut gurih.", sejarah: "Pangan pokok bersejarah masyarakat pegunungan kapur Gunungkidul dan Wonogiri sebagai pengganti beras yang tahan disimpan lama." },
      { id: 87, nama: "Gatot", asal: "DI Yogyakarta & Jatim", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Gaplek singkong terfermentasi alami hingga kehitaman, direndam, dikukus kenyal, disajikan dengan kelapa parut dan garam.", sejarah: "Berasal dari Gunungkidul; konon akronim gagal total saat singkong jemuran terkena hujan namun setelah dikukus justru manis kenyal." },
      { id: 88, nama: "Rujak Cingur", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Cingur (mulut sapi rebus empuk), sayuran rebus, buah segar (mangga muda, bengkuang), lontong, tahu, tempe, dan bumbu petis kacang.", sejarah: "Kuliner ikonik Surabaya sejak era Majapahit yang memadukan kesegaran buah, sayuran, cingur sapi, dan petis udang Sidoarjo." },
      { id: 89, nama: "Tahu Tek", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Tahu putih goreng setengah matang, lontong, kentang rebus, tauge pendek, telur dadar, kerupuk udang, dan saus petis kacang.", sejarah: "Berasal dari Surabaya dan Lamongan; dinamai Tahu Tek dari bunyi gunting penjual tek-tek saat memotong bahan di atas piring." },
      { id: 90, nama: "Lontong Balap", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Lontong potong, tauge rebus melimpah, tahu goreng, lentho (perkedel kacang tolo), kuah kaldu bening gurih, dan sambal petis.", sejarah: "Berkembang di Wonokromo Surabaya; dinamai balap karena penjual yang memikul gentong berat berjalan cepat menuju pasar." },
      { id: 91, nama: "Nasi Krawu", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Nasi pulen beralas daun pisang, suwiran daging sapi empuk manis gurih, serundeng kelapa dua warna, dan sambal terasi pedas.", sejarah: "Dibawa perantau Madura yang menetap di Gresik abad ke-18; kata krawu bermakna mengambil lauk menggunakan tangan secara langsung." },
      { id: 92, nama: "Soto Ambengan", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Ayam kampung suwir, kuah kaldu kuning pekat berempah kunyit dan kemiri, soun, telur rebus, seledri, dan bubuk koya.", sejarah: "Bermula dari warung soto legendaris di Jalan Ambengan Surabaya tahun 1970-an dengan kuah kuning pekat dan koya melimpah." },
      { id: 93, nama: "Lodho Ayam", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "daging", bahan: "Ayam kampung utuh yang dipanggang/diasap lalu dimasak dalam kuah santan kental pedas berempah kunyit, kencur, dan cabai rawit.", sejarah: "Hidangan tradisional khas Tulungagung dan Trenggalek yang biasa disajikan bersama nasi gurih dalam tradisi kenduri desa." },
      { id: 94, nama: "Pecel Lele", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "ikan", bahan: "Ikan lele segar marinasi bawang putih kunyit digoreng garing, sambal tomat terasi segar, lalapan kemangi timun, dan nasi hangat.", sejarah: "Dipopulerkan perantau asal Lamongan sejak 1970-an melalui warung tenda kaki lima hingga menjadi kuliner malam paling merakyat." },
      { id: 95, nama: "Bubur Pedas", asal: "Kalimantan Barat", wilayah: "Kalimantan", tipe: "nasi", bahan: "Beras sangrai tumbuk halus bersama kelapa parut sangrai, puluhan sayuran hutan dan daun kesum, kacang tanah goreng, dan teri.", sejarah: "Hidangan tradisional Melayu Sambas sejak masa Kesultanan Sambas yang mencerminkan kearifan menjaga keragaman hayati hutan." },
      { id: 96, nama: "Chai Kue", asal: "Kalimantan Barat", wilayah: "Kalimantan", tipe: "kue", bahan: "Kulit tipis transparan dari tepung beras dan tapioka, isian bengkuang, kucai, talas, atau rebung dengan ebi, dikukus dan disiram minyak bawang.", sejarah: "Dibawa komunitas perantau Tionghoa Hakka dan Tiochiu di Singkawang dan Pontianak sejak abad ke-19." },
      { id: 97, nama: "Pengkang", asal: "Kalimantan Barat", wilayah: "Kalimantan", tipe: "kue", bahan: "Beras ketan dimasak santan, diisi ebi pedas manis, dibungkus daun pisang segitiga lalu dijepit bambu dan dibakar di atas bara.", sejarah: "Kuliner Melayu Pontianak dan Mempawah yang awalnya dibuat sebagai bekal tahan lama bagi petani dan nelayan." },
      { id: 98, nama: "Ketupat Kandangan", asal: "Kalimantan Selatan", wilayah: "Kalimantan", tipe: "kuah", bahan: "Ketupat beras disiram kuah santan kental berempah kayu manis, cengkeh, kapulaga, dan kunyit, dengan ikan gabus (haruan) asap.", sejarah: "Berasal dari Kota Kandangan Hulu Sungai Selatan; keunikannya pada penggunaan ikan haruan rawa yang dipanggang sebelum dimasak." },
      { id: 99, nama: "Ayam Cincane", asal: "Kalimantan Timur", wilayah: "Kalimantan", tipe: "daging", bahan: "Ayam kampung potong besar dibakar dengan olesan bumbu merah khas Samarinda dari cabai merah, kemiri, terasi, gula merah, dan santan.", sejarah: "Hidangan kehormatan masyarakat Kutai dan Samarinda yang dulunya disajikan pada pesta pernikahan adat dan penyambutan tamu agung." },
      { id: 100, nama: "Nasi Bekepor", asal: "Kalimantan Timur", wilayah: "Kalimantan", tipe: "nasi", bahan: "Nasi putih dimasak dengan minyak sayur/samin, rempah-rempah, daun kemangi, potongan ikan asin gabus, dan sambal raja Kutai.", sejarah: "Hidangan khusus para raja Kesultanan Kutai Kartanegara; kata bekepor merujuk pada cara memutar periuk tembaga di atas bara." },
      { id: 101, nama: "Gence Ruan", asal: "Kalimantan Timur", wilayah: "Kalimantan", tipe: "ikan", bahan: "Ikan gabus (haruan) segar dibakar polos lalu disiram tumisan sambal kasar bawang merah, cabai merah, terasi, dan asam jawa.", sejarah: "Hidangan khas suku Kutai di sepanjang Sungai Mahakam dengan teknik membakar ikan polos agar rasa manis daging ikan terjaga." },
      { id: 102, nama: "Kepiting Soka", asal: "Kalimantan Utara", wilayah: "Kalimantan", tipe: "ikan", bahan: "Kepiting bakau cangkang lunak (soka) khas Tarakan digoreng tepung renyah dan dimasak saus lada hitam, saus padang, atau telur asin.", sejarah: "Berkembang di Tarakan sebagai pusat budidaya kepiting bakau yang dipanen tepat saat berganti kulit sehingga seluruhnya bisa dimakan." },
      { id: 103, nama: "Tinutuan", asal: "Sulawesi Utara", wilayah: "Sulawesi", tipe: "nasi", bahan: "Beras, labu kuning, singkong, jagung manis pipil, bayam, kangkung, daun gedi, kemangi, ikan cakalang fufu, dan sambal roa.", sejarah: "Bubur khas Manado yang melambangkan kerukunan dan kesehatan dengan memadukan aneka sayuran kebun bergizi tinggi." },
      { id: 104, nama: "Ayam Woku", asal: "Sulawesi Utara", wilayah: "Sulawesi", tipe: "daging", bahan: "Daging ayam potong, daun woku (pandan, kunyit, jeruk, serai, kemangi), kunyit, jahe, bawang merah, dan cabai rawit melimpah.", sejarah: "Berasal dari budaya kuliner Minahasa; kata woku merujuk pada daun woka yang dahulu digunakan membungkus masakan aromatik." },
      { id: 105, nama: "Cakalang Fufu", asal: "Sulawesi Utara", wilayah: "Sulawesi", tipe: "ikan", bahan: "Ikan cakalang segar dibelah dua, dijepit kerangka bambu, dibumbui garam dan rempah, lalu diasap di atas bara sabut kelapa.", sejarah: "Teknik pengawetan ikan tradisional nelayan Minahasa dan Bitung (fufu berarti diasap) agar tangkapan laut tahan disimpan lama." },
      { id: 106, nama: "Paniki", asal: "Sulawesi Utara", wilayah: "Sulawesi", tipe: "daging", bahan: "Daging kelelawar pemakan buah (paniki) bersih, santan kelapa kental, cabai rawit, bawang merah, serai, daun jeruk, dan daun pandan.", sejarah: "Kuliner tradisional masyarakat Minahasa yang diwariskan turun-temurun sebagai hidangan pesta adat dengan bumbu santan pedas." },
      { id: 107, nama: "Ayam Rica-rica", asal: "Sulawesi Utara", wilayah: "Sulawesi", tipe: "daging", bahan: "Daging ayam potong, cabai merah dan cabai rawit giling kasar melimpah, jahe, serai, daun jeruk purut, bawang merah, dan jeruk nipis.", sejarah: "Dalam bahasa Manado rica berarti cabai; lahir dari kecintaan masyarakat Minahasa terhadap cita rasa pedas segar." },
      { id: 108, nama: "Pallubasa", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kuah", bahan: "Daging dan jeroan sapi, kelapa parut sangrai halus, serai, lengkuas, kayu manis, cengkeh, jintan, dan kuning telur mentah (alas).", sejarah: "Berkembang di Makassar abad ke-20 yang memperkaya olahan jeroan dan daging sapi dengan kelapa sangrai gurih." },
      { id: 109, nama: "Sop Konro", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kuah", bahan: "Iga sapi ukuran besar, kluwek pewarna kuah cokelat gelap, kayu manis, cengkeh, kapulaga, jintan, serai, dan buras/ketupat.", sejarah: "Diciptakan Haji Hanaping di Makassar tahun 1960-an yang mengolah tulang iga sapi menjadi sup berempah pekat kaya kolagen." },
      { id: 110, nama: "Konro Bakar", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "daging", bahan: "Iga sapi rebus empuk berbumbu konro dibakar dengan olesan bumbu kacang manis gurih, disajikan bersama semangkuk kuah kaldu konro.", sejarah: "Inovasi modern dari Sop Konro tradisional di Makassar akhir abad ke-20 yang memadukan aroma panggangan bara api dan saus kacang." },
      { id: 111, nama: "Sop Saudara", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kuah", bahan: "Daging sapi potong dadu, paru sapi goreng renyah, bihun, perkedel kentang, kuah kaldu berempah pala kayu manis, dan bawang goreng.", sejarah: "Diciptakan Haji Dollahi dari Pangkep tahun 1957 sebagai wujud harapan agar pengunjung merasa seperti saudara kandung." },
      { id: 112, nama: "Mie Titi", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "mie", bahan: "Mie telur tipis digoreng kering renyah, disiram kuah kental kaldu ayam berisi ayam suwir, udang, cumi, hati ayam, dan sawi hijau.", sejarah: "Dipopulerkan Ang Kho Tjao di Makassar tahun 1970-an dan diteruskan anaknya (Titi); menjadi akulturasi mie kering Tionghoa-Makassar." },
      { id: 113, nama: "Barongko", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kue", bahan: "Pisang kepok matang dihaluskan, telur ayam, santan kelapa, gula pasir, sedikit garam, dan pembungkus daun pisang kukus.", sejarah: "Kue tradisional sakral masyarakat Bugis-Makassar yang dahulu hanya disajikan untuk para raja pada upacara adat besar." },
      { id: 114, nama: "Jalangkote", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kue", bahan: "Kulit pastel tipis renyah, isian wortel, kentang, tauge, bihun, daging cincang, telur rebus, dan saus cair cabai cuka bawang putih.", sejarah: "Terinspirasi kue pastel pengaruh Portugis dan Belanda di pelabuhan Makassar lalu diadaptasi dengan saus cair pedas asam." },
      { id: 115, nama: "Kaledo", asal: "Sulawesi Tengah", wilayah: "Sulawesi", tipe: "kuah", bahan: "Tulang kaki lembu (sapi) berisi sumsum lembut, asam jawa muda, cabai rawit hijau utuh, serai, garam, dan singkong rebus (kasubi).", sejarah: "Berasal dari suku Kaili di Donggala dan Palu; Kaledo bermakna tulang kaki lembu yang dimasak hingga tidak keras lagi." },
      { id: 116, nama: "Uta Dada", asal: "Sulawesi Tengah", wilayah: "Sulawesi", tipe: "daging", bahan: "Ayam kampung bakar, santan kelapa kental, bawang merah, bawang putih, cabai rawit, serai, kunyit, dan daun jeruk.", sejarah: "Hidangan tradisional suku Kaili di Palu; dalam bahasa Kaili uta berarti kuah dan dada berarti santan." },
      { id: 117, nama: "Ayam Iloni", asal: "Gorontalo", wilayah: "Sulawesi", tipe: "daging", bahan: "Ayam kampung potong dimasak bersama santan dan bumbu halus (bawang, kemiri, kunyit, jahe, serai, daun pandan) sebelum dibakar.", sejarah: "Kuliner kebanggaan Gorontalo yang memadukan teknik ungkep santan dan pembakaran agar bumbu meresap hingga ke tulang." },
      { id: 118, nama: "Binte Biluhuta", asal: "Gorontalo", wilayah: "Sulawesi", tipe: "kuah", bahan: "Jagung manis pipil, ikan cakalang suwir atau udang segar, parutan kelapa muda, daun kemangi, bawang merah, cabai rawit, dan jeruk nipis.", sejarah: "Dikenal sebagai Milu Siram; menurut sejarah Gorontalo hidangan ini diciptakan untuk mendamaikan dua kerajaan yang bertikai." },
      { id: 119, nama: "Sinonggi", asal: "Sulawesi Tenggara", wilayah: "Sulawesi", tipe: "nasi", bahan: "Pati sagu murni diseduh air panas mendidih hingga menjadi gel kenyal transparan, disantap bersama ikan palumara dan sayur bening.", sejarah: "Makanan pokok tradisional suku Tolaki di Kendari dan Konawe dengan tradisi makan bersama yang disebut mosonggi." },
      { id: 120, nama: "Kabuto", asal: "Sulawesi Tenggara", wilayah: "Sulawesi", tipe: "kue", bahan: "Ubi kayu (singkong) yang dikeringkan dan difermentasi alami, dikukus empuk, disajikan dengan kelapa parut gurih dan ikan asin.", sejarah: "Pangan pokok bersejarah masyarakat Pulau Muna dan Buton sebagai ketahanan pangan tradisional menghadapi kemarau panjang." },
      { id: 121, nama: "Bau Peapi", asal: "Sulawesi Barat", wilayah: "Sulawesi", tipe: "ikan", bahan: "Ikan tongkol atau tuna segar, bawang mandar, asam mangga kering, kunyit bubuk, cabai rawit, merica, dan minyak kelapa Mandar.", sejarah: "Hidangan bahari warisan pelaut suku Mandar; dimasak dengan minyak kelapa dan asam mangga agar tahan dibawa berlayar." },
      { id: 122, nama: "Jepa", asal: "Sulawesi Barat", wilayah: "Sulawesi", tipe: "kue", bahan: "Singkong parut yang diperas airnya dan dicampur kelapa parut muda, dipanggang pipih bundar di atas wajan tanah liat (panjepang).", sejarah: "Roti tradisional masyarakat suku Mandar yang menjadi bekal wajib pelaut Sandeq saat mengarungi lautan karena padat gizi." },
      { id: 123, nama: "Ayam Taliwang", asal: "Nusa Tenggara Barat", wilayah: "Bali & Nusa Tenggara", tipe: "daging", bahan: "Ayam kampung muda utuh dibelah dan dibakar dengan bumbu pedas Lombok dari cabai merah kering, cabai rawit, terasi Lombok, dan kencur.", sejarah: "Berasal dari Kampung Karang Taliwang Mataram; tercipta saat pasukan Kerajaan Taliwang Sumbawa membantu Kerajaan Selaparang." },
      { id: 124, nama: "Plecing Kangkung", asal: "Nusa Tenggara Barat", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Kangkung air khas Lombok berbatang besar renyah direbus sebentar, tauge, kacang tanah goreng, dan sambal tomat terasi jeruk limau.", sejarah: "Pendamping wajib Ayam Taliwang yang memanfaatkan kualitas air mata air pegunungan Rinjani sehingga kangkung renyah segar." },
      { id: 125, nama: "Beberuk Terong", asal: "Nusa Tenggara Barat", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Terong bulat ungu/hijau mentah potong dadu, kacang panjang iris mentah, bawang merah, tomat, dan sambal terasi jeruk limau.", sejarah: "Lalapan segar khas suku Sasak di Lombok yang disajikan mentah untuk menyeimbangkan cita rasa hidangan bakar." },
      { id: 126, nama: "Sate Bulayak", asal: "Nusa Tenggara Barat", wilayah: "Bali & Nusa Tenggara", tipe: "sate", bahan: "Sate daging sapi atau ayam dengan bumbu kacang sangrai berempah santan, disajikan bersama bulayak (lontong lilit daun aren spiral).", sejarah: "Kuliner tradisional masyarakat Sasak di Lombok Barat; bentuk spiral bulayak memudahkan memakannya tanpa sendok." },
      { id: 127, nama: "Se'i Sapi", asal: "Nusa Tenggara Timur", wilayah: "Bali & Nusa Tenggara", tipe: "daging", bahan: "Daging sapi has dalam iris memanjang diasapi menggunakan bara kayu pohon kosambi, disajikan bersama sambal lu'at dan daun pepaya.", sejarah: "Berasal dari tradisi masyarakat Pulau Timor dan Rote (se'i berarti daging tipis memanjang); pengasapan kayu kosambi mengawetkan daging." },
      { id: 128, nama: "Jagung Bose", asal: "Nusa Tenggara Timur", wilayah: "Bali & Nusa Tenggara", tipe: "nasi", bahan: "Jagung putih kering tumbuk, kacang merah, kacang tanah, santan kelapa, dan sedikit garam.", sejarah: "Pangan pokok tradisional masyarakat Timor di NTT yang kaya serat dan protein nabati, lahir dari adaptasi iklim sabana kering." },
      { id: 129, nama: "Ikan Kuah Kuning", asal: "Maluku & Papua", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Ikan tongkol, kakap, atau mubara segar, kunyit segar, jahe, lengkuas, serai, daun kemangi, cabai rawit, dan jeruk nipis tanpa santan.", sejarah: "Kuliner bahari utama Maluku dan Papua yang selalu menjadi pasangan sejati Papeda dengan kuah rempah segar tanpa santan." },
      { id: 130, nama: "Pagit-pagit", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "kuah", bahan: "Sari rumput muda lambung sapi/kerbau (teritip), daging sapi, kikil, daun singkong, rimbang, santan, dan rempah khas Karo.", sejarah: "Kuliner tradisional suku Batak Karo (terites) yang dahulu hanya disajikan pada pesta adat besar sebagai penghormatan tamu." },
      { id: 131, nama: "Naniura", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "ikan", bahan: "Ikan mas segar tanpa sisik dan duri dimatangkan alami dengan asam jungga, andaliman, kecombrang, kemiri sangrai, dan kunyit.", sejarah: "Dijuluki Sashimi Batak; pada masa lalu Naniura merupakan hidangan eksklusif yang hanya disantap raja-raja Batak di Danau Toba." },
      { id: 132, nama: "Dali ni Horbo", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "kue", bahan: "Susu kerbau murni direbus dengan air perasan nanas atau daun pepaya hingga menggumpal padat seperti keju lembut.", sejarah: "Warisan kuliner tradisional Tapanuli Utara yang mengolah susu kerbau lokal menjadi produk keju tradisional bergizi tinggi." },
      { id: 133, nama: "Manuk Napinadar", asal: "Sumatera Utara", wilayah: "Sumatera", tipe: "daging", bahan: "Ayam kampung bakar, andaliman, bawang putih, bawang merah, kemiri sangrai, lengkuas, dan saus bumbu pekat tradisi Batak.", sejarah: "Hidangan adat masyarakat Batak Toba pada acara syukuran keluarga atau pemberangkatan perantau sebagai simbol doa keselamatan." },
      { id: 134, nama: "Anyang Pakis", asal: "Sumatera Utara & Riau", wilayah: "Sumatera", tipe: "sayur", bahan: "Pucuk daun pakis rebus, kelapa parut sangrai berbumbu, bawang merah iris, serai iris halus, cabai rawit, dan jeruk nipis.", sejarah: "Salad tradisional masyarakat Melayu pesisir Sumatera Timur dan Riau yang memanfaatkan pakis liar tepian sungai." },
      { id: 135, nama: "Gulai Tepek Ikan", asal: "Jambi", wilayah: "Sumatera", tipe: "ikan", bahan: "Pempek ikan gabus/tenggiri potong pipih (tepek), santan kelapa, nanas potong, kunyit, lengkuas, serai, kemiri, dan cabai merah.", sejarah: "Hidangan prestisius Melayu Jambi yang wajib hadir pada kenduri pernikahan adat dan penyambutan tamu sejak era Kesultanan." },
      { id: 136, nama: "Gulai Terjun", asal: "Jambi", wilayah: "Sumatera", tipe: "kuah", bahan: "Daging sapi atau kerbau potong, santan encer, kelapa sangrai halus, bawang merah, cabai merah, lengkuas, serai, dan asam kandis.", sejarah: "Berasal dari Sarolangun dan Merangin; dinamai Gulai Terjun karena saat kenduri daging dan bumbu langsung diterjunkan ke kuali." },
      { id: 137, nama: "Gabus Pucung", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "ikan", bahan: "Ikan gabus segar goreng, kluwek (pucung) pewarna hitam gurih, bawang merah, kemiri, kunyit, jahe, serai, dan cabai rawit.", sejarah: "Kuliner klasik Betawi yang menjadi hidangan wajib dalam tradisi nyorog (mengantar makanan ke orang tua menjelang Ramadan)." },
      { id: 138, nama: "Sayur Babanci", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "kuah", bahan: "Daging kepala sapi, kelapa muda kerok, santan, serta 21 jenis rempah dan akar langka (kedaung, botor, lempuyang, adas).", sejarah: "Kuliner Betawi langka yang dinamai Babanci karena bukan gulai, bukan soto, dan tidak memakai sayuran hijau sama sekali." },
      { id: 139, nama: "Kue Dongkal", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Tepung beras tumbuk kasar, kelapa parut setengah tua, gula aren sisir berlapis di tengah, daun pandan, dikukus dalam aseupan.", sejarah: "Kue tradisional Betawi kuno yang dikukus dalam cetakan bambu kerucut menghasilkan lelehan gula aren manis di setiap lapisan." },
      { id: 140, nama: "Geplak Bakar", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Tepung beras sangrai, kelapa parut sangrai, gula pasir, santan kental, dan daun pandan yang dipadatkan lalu dipanggang.", sejarah: "Kudapan tradisional Betawi yang selalu hadir sebagai seserahan wajib dalam prosesi lamaran dan pernikahan adat Betawi." },
      { id: 141, nama: "Bubur Ase", asal: "DKI Jakarta", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Bubur nasi putih lembut, kuah semur daging sapi dan kentang cokelat gelap, tauge segar, asinan sawi, kedelai goreng, dan kerupuk.", sejarah: "Akulturasi Betawi dan Tionghoa; kata ase berasal dari bahasa Betawi hase yang berarti kuah semur daging dingin." },
      { id: 142, nama: "Botok Tawon", asal: "Jawa Timur", wilayah: "Jawa & Jakarta", tipe: "sayur", bahan: "Sarang lebah (tawon) muda berisi larva lebah, kelapa parut muda, bawang merah, bawang putih, cabai rawit, belimbing wuluh, dan daun pisang.", sejarah: "Kuliner unik Banyuwangi dan Kediri yang lahir dari tradisi masyarakat pedesaan sekitar hutan memanfaatkan sarang lebah madu." },
      { id: 143, nama: "Growol", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Singkong kupas direndam beberapa hari hingga terfermentasi alami, diperas, ditumbuk halus, dikukus, disajikan dengan kelapa parut.", sejarah: "Makanan pokok tradisional masyarakat Kulon Progo Yogyakarta yang rendah indeks glikemik dan tahan lama." },
      { id: 144, nama: "Belalang Goreng", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "daging", bahan: "Belalang kayu segar bersih, bawang putih, ketumbar, garam, dan cabai rawit untuk varian pedas, digoreng hingga sangat renyah.", sejarah: "Berasal dari Gunungkidul; awalnya warga menangkap belalang kayu untuk melindungi tanaman pertanian lalu mengolahnya jadi camilan." },
      { id: 145, nama: "Jadah Tempe", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Jadah (ketan putih tumbuk kukus kelapa parut gurih) disantap bertumpuk bersama tempe bacem manis cokelat gula Jawa.", sejarah: "Dipopulerkan Mbah Carik di Kaliurang lereng Merapi tahun 1950-an; dikenal sebagai kudapan favorit Sri Sultan Hamengkubuwono IX." },
      { id: 146, nama: "Sate Kere", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "sate", bahan: "Tempe gembus (ampas tahu fermentasi) dan jeroan sapi dibumbui bacem lalu dibakar di atas arang, disiram sambal kacang dan lontong.", sejarah: "Lahir di Solo masa kolonial ketika rakyat kecil berkreasi membuat sate dari tempe gembus dengan cita rasa yang lezat." },
      { id: 147, nama: "Sate Klathak", asal: "DI Yogyakarta", wilayah: "Jawa & Jakarta", tipe: "sate", bahan: "Daging kambing muda segar berbumbu garam dan merica, ditusuk jeruji besi sepeda, dibakar dan disajikan dengan kuah gulai encer.", sejarah: "Berasal dari Pleret Bantul; jeruji besi sepeda menghantarkan panas ke dalam daging, nama klathak dari bunyi garam meletup." },
      { id: 148, nama: "Ndas Borok", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Singkong parut, kelapa parut muda, gula merah sisir, tepung tapioka, dan garam yang dikukus dalam loyang hingga matang legit.", sejarah: "Kue tradisional Temanggung dan Wonosobo dengan taburan gula merah di permukaannya yang manis gurih." },
      { id: 149, nama: "Bongko Mento", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Dadar tepung terigu tipis membungkus tumisan suwiran ayam, jamur kuping, soun, dan areh santan kental, dibungkus daun pisang kukus.", sejarah: "Kuliner klasik warisan Keraton Jepara dan Solo yang memadukan kelembutan dadar gulung dengan isian gurih bersantan." },
      { id: 150, nama: "Carang Gesing", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "kue", bahan: "Pisang kepok atau raja matang potong kecil, santan kelapa, telur ayam, gula pasir, daun pandan, dan pembungkus daun pisang kukus.", sejarah: "Kudapan tradisional Solo sejak era Keraton Surakarta yang memadukan manis pisang matang dengan puding santan telur." },
      { id: 151, nama: "Horok-horok", asal: "Jawa Tengah", wilayah: "Jawa & Jakarta", tipe: "nasi", bahan: "Tepung sari pati pohon aren (enau) dikukus hingga berbentuk butiran kenyal kecil, disantap bersama pecel, bakso, atau sate kikil.", sejarah: "Pangan tradisional langka khas Jepara yang mengolah pati batang pohon aren menjadi butiran kenyal serbaguna." },
      { id: 152, nama: "Wadi", asal: "Kalimantan Tengah & Selatan", wilayah: "Kalimantan", tipe: "ikan", bahan: "Ikan air tawar (patin, gabus, baung) atau daging difermentasi bersama garam dan samu (beras sangrai tumbuk), lalu digoreng.", sejarah: "Teknik pengawetan pangan kuno suku Dayak dan Banjar agar ikan sungai saat musim surut dapat disimpan berbulan-bulan." },
      { id: 153, nama: "Juhu Umbut Rotan", asal: "Kalimantan Tengah", wilayah: "Kalimantan", tipe: "sayur", bahan: "Umbut rotan (ujung batang rotan muda empuk), ikan baung atau patin sungai, terong asam rimbang, kunyit, lengkuas, dan serai.", sejarah: "Hidangan kebanggaan suku Dayak Ngaju yang memanfaatkan tunas muda rotan hutan dengan perpaduan rasa pahit ringan dan asam gurih." },
      { id: 154, nama: "Kalumpe", asal: "Kalimantan Tengah", wilayah: "Kalimantan", tipe: "sayur", bahan: "Daun singkong muda ditumbuk halus bersama bawang merah, bawang putih, serai, lengkuas, terong pipit, dan ikan teri/udang kering.", sejarah: "Sayur tradisional suku Dayak Ma'anyan dan Ngaju (karuang); daun singkong ditumbuk halus agar lembut menyatu dengan rempah." },
      { id: 155, nama: "Hintalu Karuang", asal: "Kalimantan Selatan", wilayah: "Kalimantan", tipe: "kue", bahan: "Bola-bola kecil adonan tepung ketan dan air kapur sirih direbus dalam kuah santan kental manis gula aren, kayu manis, dan pandan.", sejarah: "Kudapan manis suku Banjar; namanya berarti telur burung karuang, merujuk pada bentuk bulatan ketan di dalam kuah gula merah." },
      { id: 156, nama: "Lawar Klungah", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Klungah (sabut dalam kelapa masih sangat muda empuk) dicincang halus, kelapa parut sangrai, daging cincang, dan base genep Bali.", sejarah: "Variasi istimewa lawar tradisional Bali yang memanfaatkan bagian dalam kelapa muda (klungah) sehingga renyah segar." },
      { id: 157, nama: "Jukut Ares", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Ares (batang pohon pisang muda bagian dalam diiris tipis), kaldu tulang ayam atau bebek, base genep lengkap, daun salam, dan serai.", sejarah: "Hidangan wajib dalam tradisi megibung (makan bersama) dan upacara adat Bali dengan memanfaatkan batang pohon pisang muda." },
      { id: 158, nama: "Bubur Mengguh", asal: "Bali", wilayah: "Bali & Nusa Tenggara", tipe: "nasi", bahan: "Bubur beras gurih santan, ayam suwir berbumbu rempah Bali, kacang tanah goreng, seledri, bawang goreng, dan urap sayuran.", sejarah: "Kuliner tradisional khas Kabupaten Buleleng (Bali Utara) yang disajikan saat upacara adat maupun sarapan hangat bergizi." },
      { id: 159, nama: "Catemak Jagung", asal: "Nusa Tenggara Timur", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Jagung pipil, labu lilin, kacang hijau, kacang tanah, bunga pepaya, daun marungga (kelor), dan garam tanpa santan.", sejarah: "Hidangan tradisional masyarakat Kupang dan Timor yang memadukan aneka biji-bijian serta sayuran lokal tahan kering." },
      { id: 160, nama: "Rumpu Rampe", asal: "Nusa Tenggara Timur", wilayah: "Bali & Nusa Tenggara", tipe: "sayur", bahan: "Bunga pepaya, daun pepaya muda, jantung pisang, daun singkong, dan daun kelor ditumis bersama bawang merah, cabai rawit, dan terasi.", sejarah: "Sayur tumis khas Flores dan Maumere yang mengolah sayuran pahit menjadi hidangan lezat pendamping ikan bakar laut Flores." },
      { id: 161, nama: "Kolo", asal: "Nusa Tenggara Timur", wilayah: "Bali & Nusa Tenggara", tipe: "nasi", bahan: "Beras putih atau merah berbumbu bawang merah, serai, daun pandan, dan santan, dimasukkan ke bambu muda dan dibakar di atas bara.", sejarah: "Nasi bambu tradisional masyarakat Manggarai di Flores yang selalu disajikan dalam upacara adat Penti (syukuran panen)." },
      { id: 162, nama: "Kapurung", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kuah", bahan: "Pati sagu dibentuk bulatan kecil dalam kuah kaldu ikan/ayam asam segar (patikala/mangga muda), bayam, kangkung, jagung, dan kacang tumbuk.", sejarah: "Kuliner kebanggaan masyarakat Luwu (Palopo, Masamba) yang menyatukan sari pati sagu dengan kekayaan sayuran dan ikan segar." },
      { id: 163, nama: "Dangke", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "kue", bahan: "Susu sapi atau kerbau segar direbus dengan getah buah pepaya muda sebagai penggumpal alami, dicetak tempurung kelapa, lalu digoreng/bakar.", sejarah: "Keju tradisional khas Enrekang sejak awal abad ke-20; konon namanya dari ucapan Belanda Dank je saat mencicipi olahan susu ini." },
      { id: 164, nama: "Nasu Palekko", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "daging", bahan: "Daging bebek (itik) muda dicincang kecil, asam jawa, kunyit, lengkuas, serai, merica, bawang merah, dan cabai rawit melimpah.", sejarah: "Kuliner legendaris masyarakat Bugis di Pinrang dan Sidrap (palekko merujuk pada kuali tanah liat tempat memasaknya)." },
      { id: 165, nama: "Lawa Bale", asal: "Sulawesi Selatan", wilayah: "Sulawesi", tipe: "ikan", bahan: "Ikan teri segar atau ikan mairo dimatangkan dengan perasan jeruk nipis dan cuka, dicampur kelapa parut sangrai, cabai, dan kacang tumbuk.", sejarah: "Hidangan bahari klasik masyarakat Bugis-Makassar yang menggambarkan kedekatan nelayan pesisir dengan hasil laut segar." },
      { id: 166, nama: "Pakasam", asal: "Kalimantan Selatan", wilayah: "Kalimantan", tipe: "ikan", bahan: "Ikan air tawar kecil (sepat, papuyu, wader) difermentasi dengan garam dan beras sangrai tumbuk, lalu digoreng kering bawang cabai.", sejarah: "Warisan pengawetan ikan masyarakat Hulu Sungai (Banjar) memanfaatkan melimpahnya ikan rawa untuk cadangan lauk berbulan-bulan." },
      { id: 167, nama: "Gohu Ikan", asal: "Maluku Utara", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Ikan tuna atau cakalang segar potong dadu mentah, garam, lemon cui, irisan bawang merah, cabai rawit, kemangi, dan minyak kelapa panas.", sejarah: "Dijuluki Sashimi Ternate; hidangan laut segar khas Kesultanan Ternate yang menonjolkan kesegaran ikan tanpa pemasakan api." },
      { id: 168, nama: "Kohu-kohu", asal: "Maluku", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Ikan tongkol/cakalang asap suwir, kelapa parut setengah tua, kacang panjang iris mentah, tauge, bawang merah, cabai, dan jeruk nipis.", sejarah: "Urap khas kepulauan Maluku yang sering disantap bersama kasbi (singkong rebus) atau embal sebagai menu sehat harian." },
      { id: 169, nama: "Embal", asal: "Maluku", wilayah: "Maluku & Papua", tipe: "kue", bahan: "Singkong khusus (kasbi embal) diparut, diperas hingga hilang racun sianidanya, dijemur, lalu dicetak dan dipanggang menjadi lempengan renyah.", sejarah: "Pangan pokok tradisional Kepulauan Kei Maluku Tenggara; teknik cerdas mengubah singkong beracun menjadi biskuit tahan lama." },
      { id: 170, nama: "Ulat Sagu", asal: "Papua & Maluku", wilayah: "Maluku & Papua", tipe: "daging", bahan: "Larva kumbang sagu alami yang hidup di dalam batang pohon sagu tumbang, dibakar seperti sate atau ditumis bumbu sederhana.", sejarah: "Sumber protein alami dan lemak sehat bagi masyarakat adat Kamoro, Asmat, dan suku di Papua dari tradisi pangan hutan sagu." },
      { id: 171, nama: "Udang Selingkuh", asal: "Papua Pegunungan", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Udang air tawar endemik Sungai Baliem bercapit besar menyerupai kepiting, direbus atau dibakar bumbu bawang putih mentega dan sambal.", sejarah: "Kuliner ikonik Lembah Baliem Wamena; dinamai Udang Selingkuh secara jenaka karena bertubuh udang namun bercapit seperti kepiting." },
      { id: 172, nama: "Ikan Bungkus", asal: "Papua", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Ikan laut segar (kakap/tongkol), bawang merah, bawang putih, serai, kunyit, cabai rawit, daun kemangi, dan pembungkus daun talas bakar.", sejarah: "Pepes khas pesisir Papua (Sorong dan Manokwari) yang menggunakan daun talas sebagai pembungkus alami beraroma bakaran khas." },
      { id: 173, nama: "Aunu Senebre", asal: "Papua", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Ikan teri nasi segar digoreng kering, dicampur irisan daun talas muda dan parutan kelapa muda, lalu dikukus hingga matang lembut.", sejarah: "Hidangan tradisional pesisir Biak dan Teluk Cenderawasih yang memadukan ikan teri laut dengan daun talas pendamping papeda." },
      { id: 174, nama: "Martabak Sagu", asal: "Papua & Maluku", wilayah: "Maluku & Papua", tipe: "kue", bahan: "Tepung sagu sangrai halus dipadatkan di atas wajan panas bersama parutan kelapa muda dan gula aren sisir hingga meleleh renyah.", sejarah: "Kudapan manis tradisional masyarakat Fakfak dan pesisir Papua yang mengkreasikan tepung sagu lokal menjadi camilan renyah." },
      { id: 175, nama: "Sagu Lempeng", asal: "Maluku & Papua", wilayah: "Maluku & Papua", tipe: "kue", bahan: "Tepung sagu murni (kadang dicampur parutan kelapa dan gula merah) dipanggang dalam cetakan tanah liat (forna) hingga menjadi roti renyah.", sejarah: "Roti tradisional bersejarah Maluku dan Papua yang awet disimpan berbulan-bulan, dicelupkan ke teh hangat atau kuah ikan." },
      { id: 176, nama: "Kue Lontar", asal: "Papua", wilayah: "Maluku & Papua", tipe: "kue", bahan: "Adonan kulit pie renyah tepung terigu mentega dengan isian vla lembut susu kental manis, kuning telur melimpah, dan vanili panggang.", sejarah: "Terinspirasi Rondtart (pai bundar) warisan Belanda di Fakfak dan Manokwari yang diadaptasi masyarakat Papua menjadi kue hari raya." },
      { id: 177, nama: "Sinole", asal: "Papua & Maluku", wilayah: "Maluku & Papua", tipe: "kue", bahan: "Tepung sagu kering disangrai bersama parutan kelapa muda dan sedikit garam hingga berbutir gurih (sering ditambah gula merah).", sejarah: "Pangan tradisional praktis masyarakat Papua dan Maluku yang mudah dibuat sebagai bekal perjalanan berkebun atau berburu." },
      { id: 178, nama: "Aunuve Habre", asal: "Papua", wilayah: "Maluku & Papua", tipe: "ikan", bahan: "Ikan cakalang atau tongkol segar, asam jawa, bawang merah, bawang putih, cabai rawit, dan pembungkus daun talas dikukus matang lembut.", sejarah: "Kuliner tradisional pesisir Papua yang mengukus ikan segar bersama asam jawa di dalam daun talas tanpa minyak." }
    ];

    // Generator Ilustrasi Visual Kuliner SVG Indonesia Modern (Anti Gagal Muat)
    function generateFoodArtwork(item) {
      const palettes = {
        daging: { bg1: "#7F1D1D", bg2: "#DC2626", accent: "#F59E0B", label: "Olahan Daging & Unggas" },
        sate:   { bg1: "#991B1B", bg2: "#EA580C", accent: "#FBBF24", label: "Sate & Panggangan Nusantara" },
        kuah:   { bg1: "#B45309", bg2: "#D97706", accent: "#FEF3C7", label: "Soto, Sup & Hidangan Berkuah" },
        nasi:   { bg1: "#9A3412", bg2: "#DC2626", accent: "#FDE68A", label: "Hidangan Nasi & Sagu Pokok" },
        ikan:   { bg1: "#0F172A", bg2: "#B91C1C", accent: "#38BDF8", label: "Kuliner Bahari & Ikan Nusantara" },
        sayur:  { bg1: "#14532D", bg2: "#15803D", accent: "#FBBF24", label: "Sayuran, Urap & Salad Lokal" },
        mie:    { bg1: "#991B1B", bg2: "#B45309", accent: "#FDE047", label: "Olahan Mie Tradisional" },
        kue:    { bg1: "#831843", bg2: "#DC2626", accent: "#FCD34D", label: "Kue, Jajanan & Kudapan" }
      };

      const p = palettes[item.tipe] || palettes.daging;

      const icons = {
        sate: `<g stroke="#FEF3C7" stroke-width="4" stroke-linecap="round">
                <line x1="110" y1="155" x2="290" y2="85"/>
                <line x1="110" y1="185" x2="290" y2="115"/>
                <rect x="145" y="122" width="24" height="16" rx="6" transform="rotate(-21 145 122)" fill="#F59E0B"/>
                <rect x="185" y="106" width="24" height="16" rx="6" transform="rotate(-21 185 106)" fill="#FDE68A"/>
                <rect x="225" y="90" width="24" height="16" rx="6" transform="rotate(-21 225 90)" fill="#F59E0B"/>
                <rect x="145" y="152" width="24" height="16" rx="6" transform="rotate(-21 145 152)" fill="#FDE68A"/>
                <rect x="185" y="136" width="24" height="16" rx="6" transform="rotate(-21 185 136)" fill="#F59E0B"/>
                <rect x="225" y="120" width="24" height="16" rx="6" transform="rotate(-21 225 120)" fill="#FDE68A"/>
              </g>`,
        kuah: `<g>
                <path d="M125 125 Q125 190 200 190 Q275 190 275 125 Z" fill="#FFFFFF" fill-opacity="0.95"/>
                <ellipse cx="200" cy="125" rx="75" ry="16" fill="#F59E0B"/>
                <path d="M170 95 Q165 80 175 68 M200 92 Q195 75 205 62 M230 95 Q225 80 235 68" stroke="#FFFFFF" stroke-width="3.5" stroke-linecap="round" fill="none" opacity="0.8"/>
              </g>`,
        nasi: `<g>
                <ellipse cx="200" cy="172" rx="92" ry="22" fill="#FFFFFF" fill-opacity="0.92"/>
                <path d="M145 168 L200 88 L255 168 Z" fill="#FBBF24"/>
                <circle cx="165" cy="164" r="12" fill="#DC2626"/>
                <circle cx="235" cy="164" r="12" fill="#16A34A"/>
              </g>`,
        ikan: `<g fill="#FFFFFF" fill-opacity="0.92">
                <path d="M125 135 Q185 85 255 135 Q185 185 125 135 Z"/>
                <polygon points="250,135 288,108 282,135 288,162" fill="#F59E0B"/>
                <circle cx="152" cy="128" r="5" fill="#0F172A"/>
              </g>`,
        sayur: `<g>
                <path d="M120 130 Q200 205 280 130 Z" fill="#FFFFFF" fill-opacity="0.94"/>
                <circle cx="165" cy="122" r="20" fill="#4ADE80"/>
                <circle cx="202" cy="116" r="24" fill="#22C55E"/>
                <circle cx="236" cy="124" r="19" fill="#FACC15"/>
              </g>`,
        mie: `<g>
                <path d="M125 135 Q125 192 200 192 Q275 192 275 135 Z" fill="#FFFFFF" fill-opacity="0.94"/>
                <path d="M140 130 Q170 112 200 130 T260 130" stroke="#FBBF24" stroke-width="6" fill="none" stroke-linecap="round"/>
                <path d="M145 142 Q175 124 205 142 T255 142" stroke="#FDE047" stroke-width="5" fill="none" stroke-linecap="round"/>
                <line x1="150" y1="88" x2="265" y2="108" stroke="#FDE68A" stroke-width="4" stroke-linecap="round"/>
                <line x1="150" y1="102" x2="265" y2="115" stroke="#FDE68A" stroke-width="4" stroke-linecap="round"/>
              </g>`,
        kue: `<g>
                <ellipse cx="200" cy="175" rx="88" ry="18" fill="#FFFFFF" fill-opacity="0.92"/>
                <rect x="145" y="115" width="110" height="52" rx="12" fill="#FBBF24"/>
                <rect x="145" y="135" width="110" height="12" fill="#DC2626"/>
                <circle cx="200" cy="105" r="10" fill="#FFFFFF"/>
              </g>`,
        daging: `<g>
                <ellipse cx="200" cy="172" rx="92" ry="20" fill="#FFFFFF" fill-opacity="0.94"/>
                <ellipse cx="200" cy="142" rx="64" ry="30" fill="#F59E0B"/>
                <circle cx="182" cy="134" r="9" fill="#DC2626"/>
                <circle cx="218" cy="136" r="8" fill="#16A34A"/>
                <circle cx="200" cy="148" r="7" fill="#FEF3C7"/>
              </g>`
      };

      const safeName = item.nama.replace(/&/g, "&amp;").replace(/</g, "&lt;");
      const safeAsal = item.asal.replace(/&/g, "&amp;").replace(/</g, "&lt;");

      const svg = `
        <svg xmlns="http://www.w3.org/2000/svg" width="400" height="280" viewBox="0 0 400 280">
          <defs>
            <linearGradient id="g" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stop-color="${p.bg1}"/>
              <stop offset="100%" stop-color="${p.bg2}"/>
            </linearGradient>
          </defs>
          <rect width="400" height="280" fill="url(#g)"/>
          <circle cx="200" cy="135" r="95" fill="#FFFFFF" fill-opacity="0.07"/>
          <circle cx="200" cy="135" r="72" fill="none" stroke="${p.accent}" stroke-width="1.5" stroke-dasharray="6 6" opacity="0.6"/>
          <rect x="14" y="14" width="372" height="252" rx="14" fill="none" stroke="#FFFFFF" stroke-opacity="0.25" stroke-width="1.5"/>
          <text x="200" y="42" text-anchor="middle" fill="${p.accent}" font-family="sans-serif" font-size="11" font-weight="700" letter-spacing="1.5">${p.label.toUpperCase()}</text>
          ${icons[item.tipe] || icons.daging}
          <text x="200" y="226" text-anchor="middle" fill="#FFFFFF" font-family="Georgia, serif" font-size="21" font-weight="bold">${safeName}</text>
          <text x="200" y="248" text-anchor="middle" fill="#FDE68A" font-family="sans-serif" font-size="12" font-weight="600">${safeAsal}</text>
        </svg>
      `;

      return "data:image/svg+xml;charset=UTF-8," + encodeURIComponent(svg);
    }

    // State Aplikasi
    let filteredList = [...makananData];
    let currentSlideIndex = 0;
    let currentRegion = "Semua";
    let searchQuery = "";
    let viewMode = "slide"; // 'slide' atau 'grid'

    // Elemen DOM
    const searchInput = document.getElementById("searchInput");
    const clearSearch = document.getElementById("clearSearch");
    const regionTabs = document.getElementById("regionTabs");
    const resultCount = document.getElementById("resultCount");
    const slideStage = document.getElementById("slideStage");
    const slideContentArea = document.getElementById("slideContentArea");
    const slideIndicator = document.getElementById("slideIndicator");
    const prevSlideBtn = document.getElementById("prevSlideBtn");
    const nextSlideBtn = document.getElementById("nextSlideBtn");
    const catalogGrid = document.getElementById("catalogGrid");
    const emptyState = document.getElementById("emptyState");
    const btnSlideView = document.getElementById("btnSlideView");
    const btnGridView = document.getElementById("btnGridView");

    function applyFilters() {
      const q = searchQuery.toLowerCase().trim();
      filteredList = makananData.filter((item) => {
        const matchRegion = currentRegion === "Semua" || item.wilayah === currentRegion;
        const matchQuery =
          !q ||
          item.nama.toLowerCase().includes(q) ||
          item.asal.toLowerCase().includes(q) ||
          item.wilayah.toLowerCase().includes(q) ||
          item.bahan.toLowerCase().includes(q) ||
          item.sejarah.toLowerCase().includes(q);
        return matchRegion && matchQuery;
      });

      currentSlideIndex = 0;
      renderUI();
    }

    function renderUI() {
      resultCount.textContent = `Menampilkan ${filteredList.length} dari ${makananData.length} kuliner Nusantara`;

      if (filteredList.length === 0) {
        slideStage.style.display = "none";
        catalogGrid.classList.remove("active");
        emptyState.style.display = "block";
        return;
      }

      emptyState.style.display = "none";

      if (viewMode === "slide") {
        slideStage.style.display = "block";
        catalogGrid.classList.remove("active");
        renderSlide();
      } else {
        slideStage.style.display = "none";
        catalogGrid.classList.add("active");
        renderGrid();
      }
    }

    function renderSlide() {
      const item = filteredList[currentSlideIndex];
      const imgUrl = generateFoodArtwork(item);
      const formattedId = String(item.id).padStart(3, "0");

      slideContentArea.innerHTML = `
        <div class="slide-card">
          <div class="slide-visual">
            <img src="${imgUrl}" alt="${item.nama}" />
          </div>
          <div class="slide-content">
            <div class="slide-meta">
              <span class="num-badge">#${formattedId}</span>
              <span class="origin-badge">${item.wilayah} &bull; ${item.asal}</span>
            </div>
            <h3 class="slide-food-title">${item.nama}</h3>
            <div class="info-block">
              <h4>Bahan-Bahan Utama</h4>
              <p>${item.bahan}</p>
            </div>
            <div class="info-block sejarah">
              <h4>Sejarah Terciptanya Makanan</h4>
              <p>${item.sejarah}</p>
            </div>
          </div>
        </div>
      `;

      slideIndicator.textContent = `Slide ${currentSlideIndex + 1} dari ${filteredList.length}`;
      prevSlideBtn.disabled = currentSlideIndex === 0;
      nextSlideBtn.disabled = currentSlideIndex === filteredList.length - 1;
    }

    function renderGrid() {
      catalogGrid.innerHTML = filteredList
        .map((item, idx) => {
          const imgUrl = generateFoodArtwork(item);
          const formattedId = String(item.id).padStart(3, "0");
          return `
            <div class="food-card" onclick="openInSlide(${idx})">
              <img src="${imgUrl}" alt="${item.nama}" class="food-card-img" loading="lazy" />
              <div class="food-card-body">
                <div class="food-card-top">
                  <span class="num-badge">#${formattedId}</span>
                  <span class="origin-badge">${item.asal}</span>
                </div>
                <h3 class="food-card-title">${item.nama}</h3>
                <p class="food-card-text"><strong>Bahan:</strong> ${item.bahan}</p>
                <p class="food-card-text"><strong>Sejarah:</strong> ${item.sejarah}</p>
                <div class="food-card-footer">
                  <span>Wilayah: ${item.wilayah}</span>
                  <span>Buka Slide &rarr;</span>
                </div>
              </div>
            </div>
          `;
        })
        .join("");
    }

    function openInSlide(index) {
      currentSlideIndex = index;
      viewMode = "slide";
      btnSlideView.classList.add("active");
      btnGridView.classList.remove("active");
      renderUI();
      slideStage.scrollIntoView({ behavior: "smooth", block: "center" });
    }

    function resetFilter() {
      searchQuery = "";
      searchInput.value = "";
      clearSearch.style.display = "none";
      currentRegion = "Semua";
      document.querySelectorAll(".filter-pill").forEach((b) => b.classList.remove("active"));
      document.querySelector('.filter-pill[data-region="Semua"]').classList.add("active");
      applyFilters();
    }

    // Event Listeners
    searchInput.addEventListener("input", (e) => {
      searchQuery = e.target.value;
      clearSearch.style.display = searchQuery ? "flex" : "none";
      applyFilters();
    });

    clearSearch.addEventListener("click", () => {
      searchQuery = "";
      searchInput.value = "";
      clearSearch.style.display = "none";
      applyFilters();
    });

    regionTabs.addEventListener("click", (e) => {
      if (e.target.classList.contains("filter-pill")) {
        document.querySelectorAll(".filter-pill").forEach((b) => b.classList.remove("active"));
        e.target.classList.add("active");
        currentRegion = e.target.dataset.region;
        applyFilters();
      }
    });

    btnSlideView.addEventListener("click", () => {
      viewMode = "slide";
      btnSlideView.classList.add("active");
      btnGridView.classList.remove("active");
      renderUI();
    });

    btnGridView.addEventListener("click", () => {
      viewMode = "grid";
      btnGridView.classList.add("active");
      btnSlideView.classList.remove("active");
      renderUI();
    });

    prevSlideBtn.addEventListener("click", () => {
      if (currentSlideIndex > 0) {
        currentSlideIndex--;
        renderSlide();
      }
    });

    nextSlideBtn.addEventListener("click", () => {
      if (currentSlideIndex < filteredList.length - 1) {
        currentSlideIndex++;
        renderSlide();
      }
    });

    document.addEventListener("keydown", (e) => {
      if (viewMode === "slide" && document.activeElement !== searchInput && filteredList.length > 0) {
        if (e.key === "ArrowLeft" && currentSlideIndex > 0) {
          currentSlideIndex--;
          renderSlide();
        } else if (e.key === "ArrowRight" && currentSlideIndex < filteredList.length - 1) {
          currentSlideIndex++;
          renderSlide();
        }
      }
    });

    // Inisialisasi Awal
    renderUI();
  </script>
</body>
</html>
