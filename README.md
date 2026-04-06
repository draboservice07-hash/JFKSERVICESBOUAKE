<!DOCTYPE html>
<html lang="fr">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <title>JFK SERVICE BOUAKÉ — Marché en ligne #1</title>
  <link
    href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap"
    rel="stylesheet" />
  <style>
    :root {
      --gr: #00A86B;
      --gr2: #007a4d;
      --or: #FF6B1A;
      --or2: #e05a0d;
      --wa: #25D366;
      --red: #e74c3c;
      --blue: #2563eb;
      --bg: #f4f6f8;
      --white: #ffffff;
      --dark: #0d1117;
      --card: #ffffff;
      --border: #e2e8f0;
      --border2: #cbd5e1;
      --text: #1a202c;
      --muted: #64748b;
      --light: #f8fafc;
      --shadow: 0 1px 3px rgba(0, 0, 0, .08), 0 1px 2px rgba(0, 0, 0, .06);
      --shadow-md: 0 4px 16px rgba(0, 0, 0, .1);
      --shadow-lg: 0 10px 40px rgba(0, 0, 0, .15);
    }

    *,
    *::before,
    *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0
    }

    html {
      scroll-behavior: smooth
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Plus Jakarta Sans', sans-serif;
      min-height: 100vh;
      overflow-x: hidden
    }

    a {
      text-decoration: none;
      color: inherit
    }

    button {
      cursor: pointer;
      font-family: 'Plus Jakarta Sans', sans-serif
    }

    input,
    select,
    textarea {
      font-family: 'Plus Jakarta Sans', sans-serif
    }

    /* ═══════════════════════════════════════
   TOP BAR
═══════════════════════════════════════ */
    .topbar {
      background: var(--dark);
      color: rgba(255, 255, 255, .75);
      font-size: .72rem;
      padding: 0 2%;
      height: 32px;
      display: flex;
      align-items: center;
      justify-content: space-between
    }

    .topbar-links {
      display: flex;
      gap: 18px
    }

    .topbar-links a {
      color: rgba(255, 255, 255, .65);
      font-size: .7rem;
      transition: color .2s
    }

    .topbar-links a:hover {
      color: #fff
    }

    .topbar-right {
      display: flex;
      gap: 14px;
      align-items: center
    }

    .topbar-right span {
      font-size: .7rem
    }

    /* ═══════════════════════════════════════
   MAIN NAV
═══════════════════════════════════════ */
    .main-nav {
      background: var(--gr);
      position: sticky;
      top: 0;
      z-index: 300;
      box-shadow: 0 2px 8px rgba(0, 168, 107, .3)
    }

    .nav-inner {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2%;
      height: 64px;
      display: flex;
      align-items: center;
      gap: 16px
    }

    .logo {
      font-family: 'Syne', sans-serif;
      font-weight: 800;
      font-size: 1.3rem;
      color: #fff;
      white-space: nowrap;
      cursor: pointer;
      flex-shrink: 0;
      display: flex;
      align-items: center;
      gap: 6px
    }

    .logo-dot {
      width: 8px;
      height: 8px;
      background: var(--or);
      border-radius: 50%
    }

    /* SEARCH BAR */
    .search-bar {
      flex: 1;
      max-width: 680px;
      display: flex;
      height: 42px;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 2px 8px rgba(0, 0, 0, .15)
    }

    .search-cat {
      background: #fff;
      border: none;
      border-right: 1px solid var(--border2);
      padding: 0 12px;
      font-size: .78rem;
      color: var(--muted);
      cursor: pointer;
      white-space: nowrap;
      min-width: 110px;
      -webkit-appearance: none
    }

    .search-input {
      flex: 1;
      border: none;
      padding: 0 14px;
      font-size: .9rem;
      color: var(--text);
      outline: none
    }

    .search-input::placeholder {
      color: #aab
    }

    .search-btn {
      background: var(--or);
      border: none;
      padding: 0 18px;
      color: #fff;
      font-size: 1rem;
      transition: background .2s;
      flex-shrink: 0
    }

    .search-btn:hover {
      background: var(--or2)
    }

    /* NAV RIGHT */
    .nav-actions {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-left: auto;
      flex-shrink: 0
    }

    .nav-btn {
      background: rgba(255, 255, 255, .15);
      border: none;
      color: #fff;
      padding: 7px 14px;
      border-radius: 6px;
      font-size: .82rem;
      font-weight: 600;
      transition: all .2s;
      display: flex;
      align-items: center;
      gap: 6px;
      white-space: nowrap
    }

    .nav-btn:hover {
      background: rgba(255, 255, 255, .28)
    }

    .nav-btn-solid {
      background: #fff;
      color: var(--gr);
      padding: 7px 16px;
      border-radius: 6px;
      font-size: .82rem;
      font-weight: 700;
      transition: all .2s;
      border: none;
      white-space: nowrap
    }

    .nav-btn-solid:hover {
      background: #f0fff8
    }

    .nav-icon-btn {
      background: none;
      border: none;
      color: #fff;
      font-size: 1.15rem;
      padding: 6px;
      position: relative;
      transition: opacity .2s
    }

    .nav-icon-btn:hover {
      opacity: .8
    }

    .nav-badge {
      position: absolute;
      top: -2px;
      right: -2px;
      background: var(--or);
      color: #fff;
      font-size: .58rem;
      font-weight: 700;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center
    }

    .nav-avatar-btn {
      display: flex;
      align-items: center;
      gap: 7px;
      background: rgba(255, 255, 255, .15);
      border: none;
      color: #fff;
      padding: 5px 12px 5px 6px;
      border-radius: 24px;
      font-size: .8rem;
      font-weight: 600;
      transition: all .2s;
      cursor: pointer
    }

    .nav-avatar-btn:hover {
      background: rgba(255, 255, 255, .28)
    }

    .nav-av {
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background: var(--or);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: .85rem;
      font-weight: 700;
      overflow: hidden;
      flex-shrink: 0
    }

    .nav-av img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%
    }

    /* ═══════════════════════════════════════
   CATEGORY NAV BAR
═══════════════════════════════════════ */
    .cat-nav {
      background: #fff;
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 64px;
      z-index: 200;
      box-shadow: var(--shadow)
    }

    .cat-nav-inner {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2%;
      display: flex;
      align-items: center;
      gap: 4px;
      overflow-x: auto;
      scrollbar-width: none;
      height: 44px
    }

    .cat-nav-inner::-webkit-scrollbar {
      display: none
    }

    .cat-pill {
      background: none;
      border: none;
      padding: 5px 14px;
      border-radius: 20px;
      font-size: .78rem;
      font-weight: 600;
      color: var(--muted);
      white-space: nowrap;
      transition: all .2s;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 5px
    }

    .cat-pill:hover {
      background: var(--light);
      color: var(--text)
    }

    .cat-pill.active {
      background: var(--gr);
      color: #fff
    }

    /* ═══════════════════════════════════════
   LAYOUT
═══════════════════════════════════════ */
    .page {
      display: none;
      min-height: calc(100vh - 108px)
    }

    .page.active {
      display: block
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2%
    }

    /* ═══════════════════════════════════════
   HOMEPAGE
═══════════════════════════════════════ */

    /* HERO BANNER */
    .hero-section {
      padding: 16px 0 0
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 220px 1fr 160px;
      gap: 12px;
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2%
    }

    /* LEFT SIDEBAR CATEGORIES */
    .sidebar-cats {
      background: #fff;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: var(--shadow);
      height: fit-content
    }

    .sidebar-cats-title {
      background: var(--gr);
      color: #fff;
      padding: 12px 16px;
      font-size: .82rem;
      font-weight: 700;
      display: flex;
      align-items: center;
      gap: 7px
    }

    .sidebar-cat-item {
      padding: 9px 16px;
      font-size: .8rem;
      border-bottom: 1px solid #f1f5f9;
      cursor: pointer;
      transition: all .2s;
      display: flex;
      align-items: center;
      gap: 8px;
      color: var(--text)
    }

    .sidebar-cat-item:hover {
      background: var(--light);
      color: var(--gr);
      padding-left: 20px
    }

    .sidebar-cat-item:last-child {
      border-bottom: none
    }

    /* BANNER CAROUSEL */
    .banner-area {
      border-radius: 10px;
      overflow: hidden;
      position: relative;
      height: 280px
    }

    .banner-slides {
      display: flex;
      transition: transform .5s ease;
      height: 100%
    }

    .banner-slide {
      min-width: 100%;
      height: 100%;
      position: relative;
      display: flex;
      align-items: center;
      padding: 40px;
      flex-shrink: 0
    }

    .bs1 {
      background: linear-gradient(135deg, #004d2e 0%, #00a86b 60%, #00d485 100%)
    }

    .bs2 {
      background: linear-gradient(135deg, #1a0d00 0%, #b34700 60%, #ff6b1a 100%)
    }

    .bs3 {
      background: linear-gradient(135deg, #0d1a2e 0%, #1a4080 60%, #2563eb 100%)
    }

    .banner-content {
      color: #fff;
      max-width: 55%
    }

    .banner-tag {
      background: rgba(255, 255, 255, .2);
      padding: 4px 12px;
      border-radius: 20px;
      font-size: .7rem;
      font-weight: 700;
      margin-bottom: 12px;
      display: inline-block;
      letter-spacing: 1px;
      text-transform: uppercase
    }

    .banner-title {
      font-family: 'Syne', sans-serif;
      font-size: 1.8rem;
      font-weight: 800;
      line-height: 1.15;
      margin-bottom: 8px
    }

    .banner-sub {
      font-size: .88rem;
      opacity: .85;
      margin-bottom: 18px;
      line-height: 1.5
    }

    .banner-cta {
      background: #fff;
      color: var(--gr);
      padding: 10px 22px;
      border-radius: 7px;
      font-weight: 700;
      font-size: .85rem;
      border: none;
      cursor: pointer;
      transition: transform .2s
    }

    .banner-cta:hover {
      transform: scale(1.04)
    }

    .banner-deco {
      position: absolute;
      right: 30px;
      top: 50%;
      transform: translateY(-50%);
      font-size: 7rem;
      opacity: .18
    }

    .banner-dots {
      position: absolute;
      bottom: 12px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      gap: 6px
    }

    .banner-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: rgba(255, 255, 255, .4);
      cursor: pointer;
      transition: all .3s
    }

    .banner-dot.active {
      background: #fff;
      width: 20px;
      border-radius: 4px
    }

    .banner-arrows {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 100%;
      display: flex;
      justify-content: space-between;
      padding: 0 10px;
      pointer-events: none
    }

    .banner-arrow {
      width: 32px;
      height: 32px;
      background: rgba(255, 255, 255, .25);
      border: none;
      border-radius: 50%;
      color: #fff;
      font-size: .9rem;
      cursor: pointer;
      pointer-events: all;
      transition: background .2s;
      display: flex;
      align-items: center;
      justify-content: center
    }

    .banner-arrow:hover {
      background: rgba(255, 255, 255, .45)
    }

    /* RIGHT MINI BANNERS */
    .mini-banners {
      display: flex;
      flex-direction: column;
      gap: 8px
    }

    .mini-banner {
      border-radius: 9px;
      padding: 14px;
      color: #fff;
      cursor: pointer;
      transition: transform .2s;
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: center
    }

    .mini-banner:hover {
      transform: scale(1.02)
    }

    .mb1 {
      background: linear-gradient(135deg, #7c3aed, #a855f7)
    }

    .mb2 {
      background: linear-gradient(135deg, #dc2626, #ef4444)
    }

    .mini-banner-title {
      font-size: .74rem;
      font-weight: 700;
      margin-bottom: 3px
    }

    .mini-banner-sub {
      font-size: .65rem;
      opacity: .8
    }

    .mini-banner-ico {
      font-size: 1.6rem;
      margin-bottom: 5px
    }

    /* FLASH DEALS */
    .section {
      padding: 20px 0 8px
    }

    .section-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 14px
    }

    .section-title {
      font-family: 'Syne', sans-serif;
      font-size: 1.05rem;
      font-weight: 800;
      display: flex;
      align-items: center;
      gap: 8px
    }

    .section-title .stag {
      background: var(--or);
      color: #fff;
      font-size: .62rem;
      padding: 2px 8px;
      border-radius: 4px;
      font-family: 'Plus Jakarta Sans', sans-serif;
      font-weight: 700;
      letter-spacing: .5px
    }

    .see-all {
      color: var(--gr);
      font-size: .8rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 4px;
      cursor: pointer
    }

    .see-all:hover {
      text-decoration: underline
    }

    /* COUNTDOWN */
    .flash-header {
      display: flex;
      align-items: center;
      gap: 14px;
      margin-bottom: 14px;
      flex-wrap: wrap
    }

    .countdown {
      display: flex;
      align-items: center;
      gap: 6px
    }

    .cd-unit {
      background: var(--dark);
      color: #fff;
      padding: 5px 8px;
      border-radius: 6px;
      font-family: 'Syne', sans-serif;
      font-size: 1rem;
      font-weight: 800;
      min-width: 36px;
      text-align: center
    }

    .cd-sep {
      color: var(--red);
      font-weight: 800;
      font-size: .9rem
    }

    /* PRODUCT GRID */
    .prod-grid {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 10px
    }

    .prod-grid.grid-5 {
      grid-template-columns: repeat(5, 1fr)
    }

    .prod-grid.grid-4 {
      grid-template-columns: repeat(4, 1fr)
    }

    /* PRODUCT CARD */
    .prod-card {
      background: #fff;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: var(--shadow);
      cursor: pointer;
      transition: all .25s;
      position: relative;
      border: 1px solid var(--border)
    }

    .prod-card:hover {
      box-shadow: var(--shadow-md);
      transform: translateY(-3px)
    }

    .prod-img {
      aspect-ratio: 1;
      overflow: hidden;
      background: #f8fafc;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3rem;
      position: relative
    }

    .prod-img img {
      width: 100%;
      height: 100%;
      object-fit: cover
    }

    .prod-badge {
      position: absolute;
      top: 7px;
      left: 7px;
      background: var(--red);
      color: #fff;
      font-size: .6rem;
      font-weight: 700;
      padding: 2px 7px;
      border-radius: 4px
    }

    .prod-badge.new {
      background: var(--gr)
    }

    .prod-badge.hot {
      background: var(--or)
    }

    .prod-fav {
      position: absolute;
      top: 7px;
      right: 7px;
      background: #fff;
      border: none;
      border-radius: 50%;
      width: 26px;
      height: 26px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: .85rem;
      box-shadow: var(--shadow);
      cursor: pointer;
      transition: transform .2s
    }

    .prod-fav:hover {
      transform: scale(1.15)
    }

    .prod-body {
      padding: 10px
    }

    .prod-name {
      font-size: .78rem;
      font-weight: 600;
      margin-bottom: 4px;
      line-height: 1.35;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
      color: var(--text)
    }

    .prod-price {
      font-family: 'Syne', sans-serif;
      font-size: .95rem;
      font-weight: 800;
      color: var(--or);
      margin-bottom: 3px
    }

    .prod-old {
      font-size: .7rem;
      color: var(--muted);
      text-decoration: line-through;
      margin-bottom: 4px
    }

    .prod-loc {
      font-size: .68rem;
      color: var(--muted);
      display: flex;
      align-items: center;
      gap: 3px
    }

    .prod-seller {
      font-size: .65rem;
      color: var(--gr);
      font-weight: 600;
      margin-top: 3px;
      display: flex;
      align-items: center;
      gap: 3px
    }

    .prod-wa-btn {
      width: 100%;
      background: var(--wa);
      color: #fff;
      border: none;
      padding: 7px;
      border-radius: 6px;
      font-size: .75rem;
      font-weight: 700;
      margin-top: 8px;
      transition: background .2s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 5px
    }

    .prod-wa-btn:hover {
      background: #1da851
    }

    /* STATS BANNER */
    .stats-band {
      background: linear-gradient(135deg, var(--gr), var(--gr2));
      border-radius: 12px;
      padding: 28px 32px;
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
      margin: 16px 0;
      color: #fff
    }

    .stat-item {
      text-align: center
    }

    .stat-num {
      font-family: 'Syne', sans-serif;
      font-size: 1.6rem;
      font-weight: 800;
      margin-bottom: 4px
    }

    .stat-lbl {
      font-size: .75rem;
      opacity: .8
    }

    /* CATEGORY CARDS */
    .cat-cards {
      display: grid;
      grid-template-columns: repeat(8, 1fr);
      gap: 10px
    }

    .cat-card {
      background: #fff;
      border-radius: 10px;
      padding: 14px 8px;
      text-align: center;
      cursor: pointer;
      transition: all .2s;
      border: 2px solid transparent;
      box-shadow: var(--shadow)
    }

    .cat-card:hover {
      border-color: var(--gr);
      transform: translateY(-2px)
    }

    .cat-card.active-cat {
      border-color: var(--gr);
      background: #f0fff8
    }

    .cat-card-ico {
      font-size: 1.8rem;
      margin-bottom: 7px
    }

    .cat-card-name {
      font-size: .7rem;
      font-weight: 700;
      color: var(--text);
      line-height: 1.3
    }

    .cat-card-count {
      font-size: .62rem;
      color: var(--muted);
      margin-top: 2px
    }

    /* BANNER 2 */
    .promo-grid {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 12px;
      margin: 16px 0
    }

    .promo-card {
      border-radius: 12px;
      padding: 22px;
      color: #fff;
      cursor: pointer;
      transition: transform .2s;
      overflow: hidden;
      position: relative
    }

    .promo-card:hover {
      transform: scale(1.02)
    }

    .pc1 {
      background: linear-gradient(135deg, #065f46, #059669)
    }

    .pc2 {
      background: linear-gradient(135deg, #7c2d12, #ea580c)
    }

    .pc3 {
      background: linear-gradient(135deg, #1e3a8a, #3b82f6)
    }

    .promo-ico {
      font-size: 2.5rem;
      margin-bottom: 10px
    }

    .promo-title {
      font-family: 'Syne', sans-serif;
      font-size: 1rem;
      font-weight: 800;
      margin-bottom: 5px
    }

    .promo-sub {
      font-size: .78rem;
      opacity: .85;
      line-height: 1.4
    }

    .promo-deco {
      position: absolute;
      right: -10px;
      bottom: -10px;
      font-size: 5rem;
      opacity: .12
    }

    /* TRUST SECTION */
    .trust-row {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 14px;
      margin: 20px 0
    }

    .trust-card {
      background: #fff;
      border-radius: 10px;
      padding: 20px;
      text-align: center;
      box-shadow: var(--shadow)
    }

    .trust-ico {
      font-size: 1.8rem;
      margin-bottom: 8px
    }

    .trust-title {
      font-size: .82rem;
      font-weight: 700;
      margin-bottom: 4px
    }

    .trust-sub {
      font-size: .72rem;
      color: var(--muted);
      line-height: 1.4
    }

    /* ═══════════════════════════════════════
   PRODUCT DETAIL PAGE
═══════════════════════════════════════ */
    #page-product {
      padding: 20px 0 40px
    }

    .prod-detail-grid {
      display: grid;
      grid-template-columns: 420px 1fr;
      gap: 24px;
      align-items: start
    }

    .prod-imgs {
      background: #fff;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: var(--shadow)
    }

    .prod-main-img {
      aspect-ratio: 1;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 6rem;
      background: #f8fafc;
      overflow: hidden;
      position: relative
    }

    .prod-main-img img {
      width: 100%;
      height: 100%;
      object-fit: cover
    }

    .prod-thumbs {
      display: flex;
      gap: 8px;
      padding: 10px;
      background: #fff;
      overflow-x: auto
    }

    .prod-thumb {
      width: 56px;
      height: 56px;
      border-radius: 7px;
      border: 2px solid var(--border);
      cursor: pointer;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      flex-shrink: 0;
      background: #f8fafc;
      transition: border-color .2s
    }

    .prod-thumb.active {
      border-color: var(--gr)
    }

    .prod-thumb img {
      width: 100%;
      height: 100%;
      object-fit: cover
    }

    .prod-info-panel {
      display: flex;
      flex-direction: column;
      gap: 14px
    }

    .prod-info-card {
      background: #fff;
      border-radius: 12px;
      padding: 20px;
      box-shadow: var(--shadow)
    }

    .prod-detail-price {
      font-family: 'Syne', sans-serif;
      font-size: 1.8rem;
      font-weight: 800;
      color: var(--or)
    }

    .prod-detail-name {
      font-size: 1.1rem;
      font-weight: 700;
      margin: 6px 0;
      line-height: 1.4
    }

    .prod-detail-meta {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      font-size: .78rem;
      color: var(--muted);
      margin: 8px 0
    }

    .prod-detail-meta span {
      display: flex;
      align-items: center;
      gap: 4px
    }

    .prod-detail-desc {
      font-size: .86rem;
      line-height: 1.65;
      color: var(--text)
    }

    .seller-card {
      display: flex;
      align-items: center;
      gap: 12px;
      background: #f8fafc;
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 14px
    }

    .seller-av {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background: var(--gr);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      color: #fff;
      font-weight: 700;
      overflow: hidden;
      flex-shrink: 0
    }

    .seller-av img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%
    }

    .seller-name {
      font-weight: 700;
      font-size: .88rem
    }

    .seller-badge {
      font-size: .68rem;
      color: var(--gr);
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 3px
    }

    .seller-loc {
      font-size: .72rem;
      color: var(--muted);
      margin-top: 2px
    }

    .btn-wa-big {
      width: 100%;
      background: var(--wa);
      color: #fff;
      border: none;
      padding: 14px;
      border-radius: 10px;
      font-size: .95rem;
      font-weight: 700;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      transition: background .2s;
      margin-bottom: 10px
    }

    .btn-wa-big:hover {
      background: #1da851
    }

    .btn-save {
      width: 100%;
      background: #fff;
      color: var(--text);
      border: 1.5px solid var(--border2);
      padding: 12px;
      border-radius: 10px;
      font-size: .88rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      transition: all .2s
    }

    .btn-save:hover {
      border-color: var(--gr);
      color: var(--gr)
    }

    /* ═══════════════════════════════════════
   SEARCH RESULTS PAGE
═══════════════════════════════════════ */
    #page-search {
      padding: 20px 0 40px
    }

    .search-layout {
      display: grid;
      grid-template-columns: 220px 1fr;
      gap: 16px;
      align-items: start
    }

    .filter-panel {
      background: #fff;
      border-radius: 12px;
      padding: 18px;
      box-shadow: var(--shadow)
    }

    .filter-title {
      font-weight: 700;
      font-size: .88rem;
      margin-bottom: 12px;
      padding-bottom: 8px;
      border-bottom: 1px solid var(--border)
    }

    .filter-section {
      margin-bottom: 18px
    }

    .filter-section-title {
      font-size: .78rem;
      font-weight: 700;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: .5px;
      margin-bottom: 8px
    }

    .filter-check {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 6px;
      cursor: pointer;
      font-size: .8rem
    }

    .filter-check input {
      accent-color: var(--gr);
      width: 14px;
      height: 14px
    }

    .filter-range {
      width: 100%;
      accent-color: var(--gr);
      margin-top: 4px
    }

    .search-results-area {}

    .search-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 14px;
      flex-wrap: wrap;
      gap: 8px
    }

    .results-count {
      font-size: .84rem;
      color: var(--muted)
    }

    .results-count b {
      color: var(--text)
    }

    .sort-select {
      background: #fff;
      border: 1px solid var(--border2);
      border-radius: 7px;
      padding: 6px 12px;
      font-size: .78rem;
      cursor: pointer;
      outline: none
    }

    .results-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px
    }

    /* ═══════════════════════════════════════
   DASHBOARD
═══════════════════════════════════════ */
    #page-dashboard {
      padding: 20px 0 40px
    }

    .dash-layout {
      display: grid;
      grid-template-columns: 220px 1fr;
      gap: 16px;
      align-items: start
    }

    .dash-sidebar {
      background: #fff;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: var(--shadow)
    }

    .dash-menu-item {
      padding: 12px 18px;
      font-size: .82rem;
      cursor: pointer;
      transition: all .2s;
      display: flex;
      align-items: center;
      gap: 9px;
      border-bottom: 1px solid #f1f5f9;
      color: var(--text)
    }

    .dash-menu-item:hover {
      background: var(--light);
      color: var(--gr)
    }

    .dash-menu-item.active-menu {
      background: #f0fff8;
      color: var(--gr);
      font-weight: 700;
      border-left: 3px solid var(--gr)
    }

    .dash-menu-item:last-child {
      border-bottom: none
    }

    .dash-content {
      display: flex;
      flex-direction: column;
      gap: 14px
    }

    .dash-stats-row {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 12px
    }

    .ds-card {
      background: #fff;
      border-radius: 12px;
      padding: 18px;
      box-shadow: var(--shadow)
    }

    .ds-val {
      font-family: 'Syne', sans-serif;
      font-size: 1.5rem;
      font-weight: 800;
      margin-bottom: 3px
    }

    .ds-lbl {
      font-size: .74rem;
      color: var(--muted)
    }

    .dash-ads-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px
    }

    .my-ad-card {
      background: #fff;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: var(--shadow);
      border: 1px solid var(--border)
    }

    .my-ad-img {
      aspect-ratio: 16/10;
      overflow: hidden;
      background: #f8fafc;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.5rem;
      position: relative
    }

    .my-ad-img img {
      width: 100%;
      height: 100%;
      object-fit: cover
    }

    .my-ad-body {
      padding: 12px
    }

    .my-ad-title {
      font-size: .82rem;
      font-weight: 600;
      margin-bottom: 4px;
      line-height: 1.3
    }

    .my-ad-price {
      font-family: 'Syne', sans-serif;
      font-size: .95rem;
      font-weight: 800;
      color: var(--or)
    }

    .my-ad-meta {
      font-size: .7rem;
      color: var(--muted);
      margin-top: 4px
    }

    .my-ad-actions {
      display: flex;
      gap: 6px;
      margin-top: 8px
    }

    .ad-act-btn {
      flex: 1;
      padding: 6px;
      border-radius: 6px;
      font-size: .7rem;
      font-weight: 600;
      border: 1px solid var(--border2);
      background: #fff;
      cursor: pointer;
      transition: all .2s
    }

    .ad-act-btn:hover {
      border-color: var(--gr);
      color: var(--gr)
    }

    .ad-act-del {
      border-color: var(--red);
      color: var(--red)
    }

    .ad-act-del:hover {
      background: var(--red);
      color: #fff
    }

    /* PUBLISH FORM */
    .publish-form {
      background: #fff;
      border-radius: 12px;
      padding: 24px;
      box-shadow: var(--shadow)
    }

    .pub-steps {
      display: flex;
      margin-bottom: 28px;
      gap: 0
    }

    .pub-step {
      display: flex;
      flex-direction: column;
      align-items: center;
      flex: 1;
      position: relative
    }

    .pub-step:not(:last-child)::after {
      content: '';
      position: absolute;
      top: 14px;
      left: 50%;
      width: 100%;
      height: 2px;
      background: var(--border);
      z-index: -1
    }

    .pub-step.done:not(:last-child)::after {
      background: var(--gr)
    }

    .ps-circle {
      width: 28px;
      height: 28px;
      border-radius: 50%;
      border: 2px solid var(--border);
      background: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: .72rem;
      font-weight: 700;
      color: var(--muted);
      transition: all .3s
    }

    .pub-step.ps-active .ps-circle {
      border-color: var(--gr);
      color: var(--gr);
      background: #f0fff8
    }

    .pub-step.done .ps-circle {
      border-color: var(--gr);
      background: var(--gr);
      color: #fff
    }

    .ps-label {
      font-size: .62rem;
      color: var(--muted);
      margin-top: 4px;
      text-align: center;
      font-weight: 500
    }

    .pub-step.ps-active .ps-label {
      color: var(--gr)
    }

    .pf-section {
      display: none
    }

    .pf-section.pf-active {
      display: block
    }

    .pf-title {
      font-family: 'Syne', sans-serif;
      font-size: 1rem;
      font-weight: 800;
      margin-bottom: 4px
    }

    .pf-sub {
      color: var(--muted);
      font-size: .8rem;
      margin-bottom: 20px
    }

    .fl {
      display: flex;
      gap: 12px
    }

    .fl>.fg {
      flex: 1
    }

    .fg {
      margin-bottom: 14px
    }

    .fg label {
      display: block;
      font-size: .78rem;
      font-weight: 600;
      margin-bottom: 5px;
      color: var(--muted)
    }

    .fg input,
    .fg textarea,
    .fg select {
      width: 100%;
      background: var(--light);
      border: 1.5px solid var(--border2);
      border-radius: 8px;
      padding: 10px 13px;
      font-size: .86rem;
      color: var(--text);
      outline: none;
      transition: border-color .2s
    }

    .fg input:focus,
    .fg textarea:focus,
    .fg select:focus {
      border-color: var(--gr);
      background: #f0fff8
    }

    .fg textarea {
      resize: vertical;
      min-height: 90px
    }

    .fg select {
      cursor: pointer
    }

    .photo-upload-area {
      border: 2px dashed var(--border2);
      border-radius: 10px;
      padding: 30px;
      text-align: center;
      cursor: pointer;
      transition: all .22s;
      background: var(--light)
    }

    .photo-upload-area:hover {
      border-color: var(--gr);
      background: #f0fff8
    }

    .photo-grid-upload {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
      margin-top: 12px
    }

    .photo-slot-up {
      aspect-ratio: 1;
      border: 2px dashed var(--border2);
      border-radius: 9px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: all .2s;
      background: var(--light);
      overflow: hidden;
      position: relative
    }

    .photo-slot-up:hover {
      border-color: var(--gr)
    }

    .photo-slot-up.has {
      border-color: var(--gr);
      border-style: solid
    }

    .photo-slot-up img {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 7px
    }

    .photo-slot-up .psrm {
      position: absolute;
      top: 4px;
      right: 4px;
      background: rgba(0, 0, 0, .65);
      border: none;
      border-radius: 50%;
      width: 18px;
      height: 18px;
      color: #fff;
      font-size: .6rem;
      display: none;
      align-items: center;
      justify-content: center;
      cursor: pointer
    }

    .photo-slot-up.has .psrm {
      display: flex
    }

    .pf-nav {
      display: flex;
      gap: 10px;
      margin-top: 20px
    }

    .pf-nav .btn {
      flex: 1;
      padding: 11px;
      font-size: .85rem;
      border-radius: 8px;
      text-align: center
    }

    .price-input-wrap {
      position: relative
    }

    .pcur {
      position: absolute;
      left: 12px;
      top: 50%;
      transform: translateY(-50%);
      font-size: .8rem;
      font-weight: 700;
      color: var(--or);
      pointer-events: none
    }

    .pinp {
      padding-left: 60px !important
    }

    .wa-input-group {
      display: flex
    }

    .wa-pref {
      background: #f0fff8;
      border: 1.5px solid rgba(37, 211, 102, .3);
      border-right: none;
      border-radius: 8px 0 0 8px;
      padding: 10px 11px;
      color: var(--wa);
      font-weight: 700;
      font-size: .82rem;
      display: flex;
      align-items: center;
      gap: 4px;
      white-space: nowrap;
      flex-shrink: 0
    }

    .wa-suf {
      border-radius: 0 8px 8px 0 !important;
      border-left: 1px solid rgba(37, 211, 102, .25) !important
    }

    /* ═══════════════════════════════════════
   MODALS
═══════════════════════════════════════ */
    .overlay {
      display: none;
      position: fixed;
      inset: 0;
      z-index: 600;
      background: rgba(0, 0, 0, .6);
      backdrop-filter: blur(6px);
      align-items: center;
      justify-content: center;
      padding: 16px
    }

    .overlay.open {
      display: flex
    }

    .modal {
      background: #fff;
      border-radius: 16px;
      padding: 32px;
      width: 100%;
      max-width: 440px;
      position: relative;
      animation: mdUp .3s ease;
      max-height: 90vh;
      overflow-y: auto
    }

    @keyframes mdUp {
      from {
        opacity: 0;
        transform: translateY(24px)
      }

      to {
        opacity: 1;
        transform: translateY(0)
      }
    }

    .modal-x {
      position: absolute;
      top: 14px;
      right: 14px;
      background: var(--light);
      border: none;
      border-radius: 50%;
      width: 28px;
      height: 28px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      color: var(--muted);
      transition: all .2s;
      font-size: .8rem
    }

    .modal-x:hover {
      background: var(--border);
      color: var(--text)
    }

    .modal-logo {
      font-family: 'Syne', sans-serif;
      font-weight: 800;
      font-size: 1rem;
      color: var(--gr);
      margin-bottom: 4px
    }

    .modal-title {
      font-family: 'Syne', sans-serif;
      font-size: 1.3rem;
      font-weight: 800;
      margin-bottom: 4px;
      color: var(--text)
    }

    .modal-sub {
      color: var(--muted);
      font-size: .82rem;
      margin-bottom: 20px;
      line-height: 1.5
    }

    .g-btn {
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 11px;
      background: var(--light);
      border: 1.5px solid var(--border2);
      color: var(--text);
      padding: 11px;
      border-radius: 9px;
      font-size: .86rem;
      font-weight: 600;
      cursor: pointer;
      margin-bottom: 16px;
      transition: all .2s
    }

    .g-btn:hover {
      border-color: var(--gr);
      background: #f0fff8
    }

    .g-btn svg {
      width: 18px;
      height: 18px
    }

    .div-or {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 16px;
      color: var(--muted);
      font-size: .74rem
    }

    .div-or::before,
    .div-or::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--border)
    }

    .mfg {
      margin-bottom: 13px
    }

    .mfg label {
      display: block;
      font-size: .76rem;
      font-weight: 600;
      margin-bottom: 5px;
      color: var(--muted)
    }

    .mfg input {
      width: 100%;
      background: var(--light);
      border: 1.5px solid var(--border2);
      border-radius: 8px;
      padding: 10px 13px;
      font-size: .86rem;
      color: var(--text);
      outline: none;
      transition: all .2s
    }

    .mfg input:focus {
      border-color: var(--gr);
      background: #f0fff8
    }

    .mfg input.ef {
      border-color: var(--red) !important;
      background: #fff5f5
    }

    .mfg .hint {
      font-size: .7rem;
      color: var(--muted);
      margin-top: 4px
    }

    .err-row {
      display: none;
      align-items: center;
      gap: 6px;
      background: #fff5f5;
      border: 1px solid rgba(231, 76, 60, .2);
      border-radius: 7px;
      padding: 8px 11px;
      margin-bottom: 12px;
      color: var(--red);
      font-size: .76rem
    }

    .err-row.show {
      display: flex
    }

    .pw-wrap {
      position: relative
    }

    .pw-eye {
      position: absolute;
      right: 11px;
      top: 50%;
      transform: translateY(-50%);
      background: none;
      border: none;
      color: var(--muted);
      cursor: pointer;
      font-size: .85rem;
      padding: 3px
    }

    .mfg .req-star {
      color: var(--or);
      margin-left: 2px
    }

    .modal-switch {
      text-align: center;
      font-size: .78rem;
      color: var(--muted);
      margin-top: 4px
    }

    .modal-switch a {
      color: var(--gr);
      font-weight: 600;
      cursor: pointer
    }

    .modal-switch a:hover {
      text-decoration: underline
    }

    .m-btn {
      width: 100%;
      padding: 12px;
      border-radius: 9px;
      font-size: .9rem;
      font-weight: 700;
      border: none;
      cursor: pointer;
      margin-bottom: 11px;
      transition: all .2s
    }

    .m-btn-primary {
      background: var(--gr);
      color: #fff
    }

    .m-btn-primary:hover {
      background: var(--gr2);
      transform: translateY(-1px)
    }

    .m-btn-wa {
      background: var(--wa);
      color: #fff
    }

    .m-btn-wa:hover {
      background: #1da851
    }

    .m-btn-outline {
      background: #fff;
      border: 1.5px solid var(--border2);
      color: var(--text)
    }

    .m-btn-outline:hover {
      border-color: var(--gr);
      color: var(--gr)
    }

    .forgot-a {
      display: block;
      text-align: right;
      font-size: .74rem;
      color: var(--gr);
      cursor: pointer;
      margin-top: -6px;
      margin-bottom: 12px
    }

    .forgot-a:hover {
      text-decoration: underline
    }

    /* AVATAR UPLOAD */
    .av-upload-row {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
      margin-bottom: 18px
    }

    .av-ring {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      border: 3px dashed var(--border2);
      background: var(--light);
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      position: relative;
      overflow: hidden;
      transition: border-color .2s
    }

    .av-ring:hover {
      border-color: var(--gr)
    }

    .av-ring img {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%
    }

    .av-edit-ov {
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, .5);
      display: none;
      align-items: center;
      justify-content: center;
      font-size: .65rem;
      font-weight: 600;
      color: #fff;
      border-radius: 50%;
      flex-direction: column;
      gap: 2px
    }

    .av-ring:hover .av-edit-ov {
      display: flex
    }

    .av-hint {
      font-size: .7rem;
      color: var(--muted);
      text-align: center
    }

    /* OTP */
    .otp-box {
      background: #f0fff8;
      border: 1px solid rgba(0, 168, 107, .2);
      border-radius: 10px;
      padding: 12px;
      margin-bottom: 16px;
      text-align: center;
      font-size: .84rem
    }

    .otp-num {
      font-weight: 700;
      color: var(--gr)
    }

    .otp-digits {
      display: flex;
      gap: 9px;
      justify-content: center;
      margin: 18px 0
    }

    .otp-d {
      width: 55px;
      height: 62px;
      border: 2px solid var(--border2);
      border-radius: 11px;
      text-align: center;
      font-family: 'Syne', sans-serif;
      font-size: 1.6rem;
      font-weight: 800;
      outline: none;
      background: var(--light);
      transition: all .2s;
      -moz-appearance: textfield
    }

    .otp-d::-webkit-outer-spin-button,
    .otp-d::-webkit-inner-spin-button {
      -webkit-appearance: none
    }

    .otp-d:focus {
      border-color: var(--gr);
      background: #f0fff8;
      transform: scale(1.04)
    }

    .otp-d.ok {
      border-color: var(--gr);
      background: #f0fff8
    }

    .otp-d.bad {
      border-color: var(--red);
      background: #fff5f5;
      animation: shk .35s
    }

    @keyframes shk {

      0%,
      100% {
        transform: translateX(0)
      }

      25% {
        transform: translateX(-4px)
      }

      75% {
        transform: translateX(4px)
      }
    }

    .otp-sim {
      font-size: .74rem;
      background: #fffbeb;
      border: 1px solid rgba(255, 107, 26, .2);
      border-radius: 8px;
      padding: 8px 11px;
      color: var(--or);
      margin: 8px 0;
      line-height: 1.5;
      text-align: left
    }

    .otp-timer {
      font-size: .75rem;
      color: var(--muted);
      margin: 6px 0 3px;
      text-align: center
    }

    .otp-timer b {
      color: var(--red)
    }

    .otp-resend {
      font-size: .76rem;
      color: var(--gr);
      cursor: pointer;
      text-decoration: underline;
      text-align: center;
      display: none
    }

    /* SUCCESS */
    .success-block {
      text-align: center;
      padding: 8px 0
    }

    .sb-ico {
      font-size: 2.8rem;
      margin-bottom: 11px
    }

    .sb-title {
      font-family: 'Syne', sans-serif;
      font-size: 1.25rem;
      font-weight: 800;
      margin-bottom: 6px
    }

    .sb-sub {
      color: var(--muted);
      font-size: .82rem;
      line-height: 1.55;
      margin-bottom: 16px
    }

    .profile-mini {
      display: flex;
      align-items: center;
      gap: 11px;
      background: var(--light);
      border: 1px solid var(--border);
      border-radius: 11px;
      padding: 13px;
      margin-bottom: 18px;
      text-align: left
    }

    .pm-av {
      width: 46px;
      height: 46px;
      border-radius: 50%;
      background: var(--gr);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      color: #fff;
      font-weight: 700;
      overflow: hidden;
      flex-shrink: 0;
      border: 2px solid var(--gr)
    }

    .pm-av img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%
    }

    .pm-name {
      font-weight: 700;
      font-size: .9rem
    }

    .pm-phone {
      font-size: .73rem;
      color: var(--wa);
      margin-top: 2px
    }

    .pm-email {
      font-size: .68rem;
      color: var(--muted);
      margin-top: 1px
    }

    /* PHONE PREFIX */
    .ph-wrap {
      display: flex
    }

    .ph-pfx {
      background: #f0fff8;
      border: 1.5px solid rgba(37, 211, 102, .3);
      border-right: none;
      border-radius: 8px 0 0 8px;
      padding: 10px 11px;
      color: var(--wa);
      font-weight: 700;
      font-size: .82rem;
      display: flex;
      align-items: center;
      gap: 4px;
      white-space: nowrap;
      flex-shrink: 0
    }

    .ph-sfx {
      border-radius: 0 8px 8px 0 !important;
      border-left: 1px solid rgba(37, 211, 102, .2) !important
    }

    /* TOAST */
    .toast {
      position: fixed;
      bottom: 24px;
      right: 24px;
      background: var(--dark);
      color: #fff;
      padding: 11px 20px;
      border-radius: 10px;
      font-size: .84rem;
      font-weight: 600;
      z-index: 1000;
      transform: translateY(80px);
      transition: transform .35s;
      box-shadow: var(--shadow-lg);
      max-width: 320px;
      line-height: 1.4
    }

    .toast.show {
      transform: translateY(0)
    }

    .toast.t-ok {
      background: var(--gr)
    }

    .toast.t-err {
      background: var(--red)
    }

    .toast.t-wa {
      background: var(--wa)
    }

    .toast.t-or {
      background: var(--or)
    }

    /* FOOTER */
    .footer {
      background: var(--dark);
      color: rgba(255, 255, 255, .7);
      padding: 40px 2% 20px;
      margin-top: 30px
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr 1fr;
      gap: 32px;
      max-width: 1280px;
      margin: 0 auto 28px
    }

    .footer-brand {
      font-family: 'Syne', sans-serif;
      font-size: 1.1rem;
      font-weight: 800;
      color: #fff;
      margin-bottom: 10px
    }

    .footer-brand span {
      color: var(--gr)
    }

    .footer-desc {
      font-size: .76rem;
      line-height: 1.6;
      color: rgba(255, 255, 255, .55);
      margin-bottom: 14px
    }

    .footer-col-title {
      font-size: .78rem;
      font-weight: 700;
      color: #fff;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: .5px
    }

    .footer-link {
      display: block;
      font-size: .74rem;
      color: rgba(255, 255, 255, .55);
      margin-bottom: 6px;
      cursor: pointer;
      transition: color .2s
    }

    .footer-link:hover {
      color: #fff
    }

    .footer-bottom {
      border-top: 1px solid rgba(255, 255, 255, .1);
      padding-top: 16px;
      max-width: 1280px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      font-size: .72rem;
      color: rgba(255, 255, 255, .4);
      flex-wrap: wrap;
      gap: 8px
    }

    .footer-social {
      display: flex;
      gap: 10px
    }

    .social-btn {
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background: rgba(255, 255, 255, .1);
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: background .2s;
      font-size: .85rem;
      color: #fff
    }

    .social-btn:hover {
      background: var(--gr)
    }

    /* EMPTY STATE */
    .empty-state {
      text-align: center;
      padding: 60px 20px;
      color: var(--muted)
    }

    .empty-ico {
      font-size: 3rem;
      margin-bottom: 12px
    }

    .empty-title {
      font-size: .95rem;
      font-weight: 700;
      margin-bottom: 6px;
      color: var(--text)
    }

    .empty-sub {
      font-size: .8rem;
      line-height: 1.6
    }

    /* BREADCRUMB */
    .breadcrumb {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: .76rem;
      color: var(--muted);
      margin-bottom: 14px;
      flex-wrap: wrap
    }

    .breadcrumb a {
      color: var(--gr);
      cursor: pointer
    }

    .breadcrumb a:hover {
      text-decoration: underline
    }

    .breadcrumb .sep {
      opacity: .5
    }

    /* RESPONSIVE */
    @media(max-width:1024px) {
      .prod-grid {
        grid-template-columns: repeat(4, 1fr)
      }

      .cat-cards {
        grid-template-columns: repeat(5, 1fr)
      }

      .hero-grid {
        grid-template-columns: 1fr;
      }

      .sidebar-cats {
        display: none
      }

      .mini-banners {
        display: none
      }

      .banner-area {
        border-radius: 10px
      }
    }

    @media(max-width:768px) {
      .prod-grid {
        grid-template-columns: repeat(3, 1fr)
      }

      .cat-cards {
        grid-template-columns: repeat(4, 1fr)
      }

      .stats-band {
        grid-template-columns: 1fr 1fr
      }

      .promo-grid {
        grid-template-columns: 1fr
      }

      .trust-row {
        grid-template-columns: 1fr 1fr
      }

      .search-layout {
        grid-template-columns: 1fr
      }

      .filter-panel {
        display: none
      }

      .results-grid {
        grid-template-columns: 1fr 1fr
      }

      .prod-detail-grid {
        grid-template-columns: 1fr
      }

      .dash-layout {
        grid-template-columns: 1fr
      }

      .dash-stats-row {
        grid-template-columns: 1fr 1fr
      }

      .footer-grid {
        grid-template-columns: 1fr 1fr
      }
    }

    @media(max-width:480px) {
      .prod-grid {
        grid-template-columns: repeat(2, 1fr)
      }

      .cat-cards {
        grid-template-columns: repeat(3, 1fr)
      }

      .results-grid {
        grid-template-columns: 1fr 1fr
      }

      .dash-ads-grid {
        grid-template-columns: 1fr 1fr
      }

      .nav-inner {
        gap: 8px
      }

      .search-cat {
        display: none
      }
    }
  </style>
</head>

<body>

  <!-- ════ TOP BAR ════ -->
  <div class="topbar">
    <div class="topbar-links">
      <a href="#">📍 Bouaké, Côte d'Ivoire</a>
      <a href="#">Aide &amp; Contact</a>
      <a href="#">Télécharger l'app</a>
    </div>
    <div class="topbar-right">
      <span id="tb-user-info">👋 Bienvenue sur JFK Service</span>
      <span>|</span>
      <span id="tb-date"></span>
    </div>
  </div>

  <!-- ════ MAIN NAV ════ -->
  <nav class="main-nav">
    <div class="nav-inner">
      <div class="logo" onclick="showPage('home')">
        <div class="logo-dot"></div>JFK SERVICE
      </div>
      <div class="search-bar">
        <select class="search-cat" id="search-cat-sel">
        <option value="">Toutes catégories</option>
        <option>📱 Téléphones</option><option>👗 Mode</option>
        <option>🛵 Motos</option><option>🚗 Voitures</option>
        <option>🏠 Immobilier</option><option>🛋️ Meubles</option>
        <option>🖥️ Informatique</option><option>⚽ Sport</option>
      </select>
        <input type="text" class="search-input" id="main-search" placeholder="Rechercher un article, une marque..." onkeydown="searchOnEnter(event)"/>
        <button class="search-btn" onclick="doSearch()">🔍</button>
      </div>
      <div class="nav-actions" id="nav-actions">
        <button class="nav-icon-btn" title="Favoris">❤️<span class="nav-badge" id="fav-count">0</span></button>
        <button class="nav-btn" onclick="openOverlay('login')">Se connecter</button>
        <button class="nav-btn-solid" onclick="openOverlay('signup')">S'inscrire</button>
      </div>
    </div>
  </nav>

  <!-- ════ CATEGORY NAV ════ -->
  <div class="cat-nav">
    <div class="cat-nav-inner">
      <button class="cat-pill active" onclick="filterCat('all',this)">🏠 Accueil</button>
      <button class="cat-pill" onclick="filterCat('phones',this)">📱 Téléphones</button>
      <button class="cat-pill" onclick="filterCat('mode',this)">👗 Mode</button>
      <button class="cat-pill" onclick="filterCat('motos',this)">🛵 Motos</button>
      <button class="cat-pill" onclick="filterCat('voitures',this)">🚗 Voitures</button>
      <button class="cat-pill" onclick="filterCat('immo',this)">🏠 Immobilier</button>
      <button class="cat-pill" onclick="filterCat('meubles',this)">🛋️ Meubles</button>
      <button class="cat-pill" onclick="filterCat('info',this)">🖥️ Informatique</button>
      <button class="cat-pill" onclick="filterCat('sport',this)">⚽ Sport</button>
      <button class="cat-pill" onclick="filterCat('alim',this)">🍎 Alimentation</button>
      <button class="cat-pill" onclick="filterCat('autres',this)">💼 Autres</button>
    </div>
  </div>

  <!-- ════════════════════════════════════════
     HOME PAGE
════════════════════════════════════════ -->
  <div id="page-home" class="page active">
    <div style="padding:0 0 30px">

      <!-- HERO GRID -->
      <div class="hero-section">
        <div class="hero-grid">
          <!-- Sidebar cats -->
          <div class="sidebar-cats">
            <div class="sidebar-cats-title">☰ Toutes les catégories</div>
            <div class="sidebar-cat-item" onclick="filterCat('phones',null)">📱 Téléphones &amp; Accessoires</div>
            <div class="sidebar-cat-item" onclick="filterCat('info',null)">🖥️ Informatique</div>
            <div class="sidebar-cat-item" onclick="filterCat('mode',null)">👗 Mode &amp; Vêtements</div>
            <div class="sidebar-cat-item" onclick="filterCat('motos',null)">🛵 Motos &amp; Vélos</div>
            <div class="sidebar-cat-item" onclick="filterCat('voitures',null)">🚗 Voitures</div>
            <div class="sidebar-cat-item" onclick="filterCat('immo',null)">🏠 Immobilier</div>
            <div class="sidebar-cat-item" onclick="filterCat('meubles',null)">🛋️ Meubles &amp; Maison</div>
            <div class="sidebar-cat-item" onclick="filterCat('sport',null)">⚽ Sport &amp; Loisirs</div>
            <div class="sidebar-cat-item" onclick="filterCat('alim',null)">🍎 Alimentation</div>
            <div class="sidebar-cat-item" onclick="filterCat('autres',null)">💼 Autres</div>
          </div>

          <!-- BANNER -->
          <div class="banner-area">
            <div class="banner-slides" id="banner-slides">
              <div class="banner-slide bs1">
                <div class="banner-content">
                  <div class="banner-tag">🔥 Offres du jour</div>
                  <div class="banner-title">Vendez &amp; Achetez<br>à Bouaké</div>
                  <div class="banner-sub">La plateforme #1 de Côte d'Ivoire.<br>Des milliers d'articles près de chez vous.
                  </div>
                  <button class="banner-cta" onclick="openOverlay('signup')">Commencer gratuitement →</button>
                </div>
                <div class="banner-deco">🛒</div>
              </div>
              <div class="banner-slide bs2">
                <div class="banner-content">
                  <div class="banner-tag">📱 High-Tech</div>
                  <div class="banner-title">Téléphones &amp;<br>Accessoires</div>
                  <div class="banner-sub">iPhone, Samsung, Huawei...<br>Les meilleures offres à Bouaké.</div>
                  <button class="banner-cta" style="color:var(--or)" onclick="filterCat('phones',null)">Voir les offres →</button>
                </div>
                <div class="banner-deco">📱</div>
              </div>
              <div class="banner-slide bs3">
                <div class="banner-content">
                  <div class="banner-tag">🚗 Véhicules</div>
                  <div class="banner-title">Motos, Voitures<br>&amp; Plus</div>
                  <div class="banner-sub">Trouvez votre véhicule idéal.<br>Vendeurs vérifiés, paiement en main.</div>
                  <button class="banner-cta" style="color:var(--blue)" onclick="filterCat('motos',null)">Explorer →</button>
                </div>
                <div class="banner-deco">🛵</div>
              </div>
            </div>
            <div class="banner-dots" id="banner-dots">
              <div class="banner-dot active" onclick="goBanner(0)"></div>
              <div class="banner-dot" onclick="goBanner(1)"></div>
              <div class="banner-dot" onclick="goBanner(2)"></div>
            </div>
            <div class="banner-arrows">
              <button class="banner-arrow" onclick="prevBanner()">‹</button>
              <button class="banner-arrow" onclick="nextBanner()">›</button>
            </div>
          </div>

          <!-- MINI BANNERS -->
          <div class="mini-banners">
            <div class="mini-banner mb1" onclick="openOverlay('signup')">
              <div class="mini-banner-ico">🎁</div>
              <div class="mini-banner-title">Inscription gratuite</div>
              <div class="mini-banner-sub">Publiez dès aujourd'hui</div>
            </div>
            <div class="mini-banner mb2" onclick="filterCat('mode',null)">
              <div class="mini-banner-ico">👗</div>
              <div class="mini-banner-title">Mode &amp; Style</div>
              <div class="mini-banner-sub">Nouvelles collections</div>
            </div>
          </div>
        </div>
      </div>

      <!-- CATEGORIES CARDS -->
      <div class="container">
        <div class="section">
          <div class="section-header">
            <div class="section-title">🗂️ Toutes les catégories</div>
          </div>
          <div class="cat-cards">
            <div class="cat-card" onclick="filterCat('phones',null)">
              <div class="cat-card-ico">📱</div>
              <div class="cat-card-name">Téléphones</div>
              <div class="cat-card-count" id="cnt-phones">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('mode',null)">
              <div class="cat-card-ico">👗</div>
              <div class="cat-card-name">Mode</div>
              <div class="cat-card-count" id="cnt-mode">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('motos',null)">
              <div class="cat-card-ico">🛵</div>
              <div class="cat-card-name">Motos</div>
              <div class="cat-card-count" id="cnt-motos">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('voitures',null)">
              <div class="cat-card-ico">🚗</div>
              <div class="cat-card-name">Voitures</div>
              <div class="cat-card-count" id="cnt-voitures">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('immo',null)">
              <div class="cat-card-ico">🏠</div>
              <div class="cat-card-name">Immobilier</div>
              <div class="cat-card-count" id="cnt-immo">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('meubles',null)">
              <div class="cat-card-ico">🛋️</div>
              <div class="cat-card-name">Meubles</div>
              <div class="cat-card-count" id="cnt-meubles">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('info',null)">
              <div class="cat-card-ico">🖥️</div>
              <div class="cat-card-name">Informatique</div>
              <div class="cat-card-count" id="cnt-info">0 annonces</div>
            </div>
            <div class="cat-card" onclick="filterCat('sport',null)">
              <div class="cat-card-ico">⚽</div>
              <div class="cat-card-name">Sport</div>
              <div class="cat-card-count" id="cnt-sport">0 annonces</div>
            </div>
          </div>
        </div>
      </div>

      <!-- STATS BAND -->
      <div class="container">
        <div class="stats-band">
          <div class="stat-item">
            <div class="stat-num" id="stat-users">0</div>
            <div class="stat-lbl">👤 Utilisateurs inscrits</div>
          </div>
          <div class="stat-item">
            <div class="stat-num" id="stat-ads">0</div>
            <div class="stat-lbl">📢 Annonces actives</div>
          </div>
          <div class="stat-item">
            <div class="stat-num">10+</div>
            <div class="stat-lbl">🗂️ Catégories</div>
          </div>
          <div class="stat-item">
            <div class="stat-num">100%</div>
            <div class="stat-lbl">🎁 Gratuit</div>
          </div>
        </div>
      </div>

      <!-- RECENT LISTINGS -->
      <div class="container">
        <div class="section">
          <div class="section-header">
            <div class="section-title">🆕 Annonces récentes <span class="stag">NOUVEAU</span></div>
            <div class="see-all" onclick="filterCat('all',null)">Voir tout →</div>
          </div>
          <div class="prod-grid" id="recent-grid">
            <div class="empty-state" style="grid-column:1/-1;padding:40px 0">
              <div class="empty-ico">📭</div>
              <div class="empty-title">Aucune annonce pour l'instant</div>
              <div class="empty-sub">Soyez le premier à publier une annonce !<br>Créez votre compte et commencez maintenant.
              </div>
              <button class="m-btn m-btn-primary" style="width:auto;padding:11px 24px;margin-top:14px;display:inline-block" onclick="openOverlay('signup')">+ Publier une annonce</button>
            </div>
          </div>
        </div>
      </div>

      <!-- PROMO SECTION -->
      <div class="container">
        <div class="promo-grid">
          <div class="promo-card pc1" onclick="openOverlay('signup')">
            <div class="promo-ico">🚀</div>
            <div class="promo-title">Vendez plus vite</div>
            <div class="promo-sub">Publiez gratuitement et touchez des milliers d'acheteurs à Bouaké</div>
            <div class="promo-deco">💸</div>
          </div>
          <div class="promo-card pc2" onclick="filterCat('phones',null)">
            <div class="promo-ico">📱</div>
            <div class="promo-title">High-Tech à prix doux</div>
            <div class="promo-sub">Téléphones, tablettes, accessoires... Trouvez les meilleures offres</div>
            <div class="promo-deco">⚡</div>
          </div>
          <div class="promo-card pc3">
            <div class="promo-ico">🛡️</div>
            <div class="promo-title">Transactions sécurisées</div>
            <div class="promo-sub">Vendeurs vérifiés par WhatsApp. Rencontrez-vous en sécurité</div>
            <div class="promo-deco">🔒</div>
          </div>
        </div>
      </div>

      <!-- TRUST -->
      <div class="container">
        <div class="trust-row">
          <div class="trust-card">
            <div class="trust-ico">✅</div>
            <div class="trust-title">Vendeurs vérifiés</div>
            <div class="trust-sub">Chaque vendeur vérifie son identité via WhatsApp avant de publier</div>
          </div>
          <div class="trust-card">
            <div class="trust-ico">💬</div>
            <div class="trust-title">Contact direct WhatsApp</div>
            <div class="trust-sub">Contactez directement le vendeur via WhatsApp en un clic</div>
          </div>
          <div class="trust-card">
            <div class="trust-ico">🆓</div>
            <div class="trust-title">100% Gratuit</div>
            <div class="trust-sub">Publication d'annonces entièrement gratuite, pour toujours</div>
          </div>
          <div class="trust-card">
            <div class="trust-ico">📍</div>
            <div class="trust-title">Local &amp; de confiance</div>
            <div class="trust-sub">Tous les vendeurs sont à Bouaké. Échanges en face à face</div>
          </div>
        </div>
      </div>
    </div>

    <!-- FOOTER -->
    <div class="footer">
      <div class="footer-grid">
        <div>
          <div class="footer-brand"><span>JFK</span> SERVICE BOUAKÉ</div>
          <div class="footer-desc">La première plateforme de vente en ligne de Bouaké. Achetez et vendez facilement, en
            toute confiance.</div>
          <div class="footer-social">
            <div class="social-btn">📘</div>
            <div class="social-btn">📸</div>
            <div class="social-btn">💬</div>
            <div class="social-btn">🐦</div>
          </div>
        </div>
        <div>
          <div class="footer-col-title">Liens rapides</div>
          <div class="footer-link" onclick="showPage('home')">Accueil</div>
          <div class="footer-link" onclick="filterCat('all',null)">Toutes les annonces</div>
          <div class="footer-link" onclick="openOverlay('signup')">S'inscrire</div>
          <div class="footer-link" onclick="openOverlay('login')">Se connecter</div>
        </div>
        <div>
          <div class="footer-col-title">Catégories</div>
          <div class="footer-link" onclick="filterCat('phones',null)">📱 Téléphones</div>
          <div class="footer-link" onclick="filterCat('mode',null)">👗 Mode</div>
          <div class="footer-link" onclick="filterCat('voitures',null)">🚗 Voitures</div>
          <div class="footer-link" onclick="filterCat('immo',null)">🏠 Immobilier</div>
        </div>
        <div>
          <div class="footer-col-title">Aide</div>
          <div class="footer-link">Centre d'aide</div>
          <div class="footer-link">Nous contacter</div>
          <div class="footer-link">Signaler un problème</div>
          <div class="footer-link">Conditions d'utilisation</div>
        </div>
      </div>
      <div class="footer-bottom">
        <span>© 2025 JFK Service Bouaké — Tous droits réservés</span><span>🇨🇮 Fait avec ❤️ à Bouaké</span></div>
    </div>
  </div>

  <!-- ════════════════════════════════════════
     SEARCH / BROWSE PAGE
════════════════════════════════════════ -->
  <div id="page-search" class="page">
    <div class="container">
      <div class="breadcrumb"><a
          onclick="showPage('home')">Accueil</a><span class="sep">›</span><span id="srch-breadcrumb">Résultats</span>
      </div>
      <div class="search-layout">
        <div class="filter-panel">
          <div class="filter-title">🔧 Filtres</div>
          <div class="filter-section">
            <div class="filter-section-title">Catégorie</div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="all" checked onchange="applyFilters()"/><span>Toutes</span></div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="phones" onchange="applyFilters()"/><span>📱 Téléphones</span></div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="mode" onchange="applyFilters()"/><span>👗 Mode</span></div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="motos" onchange="applyFilters()"/><span>🛵 Motos</span></div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="voitures" onchange="applyFilters()"/><span>🚗 Voitures</span></div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="immo" onchange="applyFilters()"/><span>🏠 Immobilier</span></div>
            <div class="filter-check">
              <input type="radio" name="fcat" value="meubles" onchange="applyFilters()"/><span>🛋️ Meubles</span></div>
          </div>
          <div class="filter-section">
            <div class="filter-section-title">Prix max (FCFA)</div>
            <input type="range" class="filter-range" id="price-range" min="0" max="5000000" step="10000" value="5000000" oninput="updatePriceLabel(this)"/>
            <div style="font-size:.75rem;color:var(--muted);margin-top:4px">Jusqu'à :
              <b id="price-label">5 000 000 FCFA</b></div>
          </div>
          <div class="filter-section">
            <div class="filter-section-title">Trier par</div>
            <div class="filter-check">
              <input type="radio" name="fsort" value="recent" checked onchange="applyFilters()"/><span>Plus récent</span>
            </div>
            <div class="filter-check">
              <input type="radio" name="fsort" value="price-asc" onchange="applyFilters()"/><span>Prix croissant</span>
            </div>
            <div class="filter-check">
              <input type="radio" name="fsort" value="price-desc" onchange="applyFilters()"/><span>Prix décroissant</span>
            </div>
          </div>
          <button class="m-btn m-btn-primary" style="width:100%;padding:10px;font-size:.82rem" onclick="applyFilters()">Appliquer les filtres</button>
        </div>
        <div class="search-results-area">
          <div class="search-top">
            <div class="results-count" id="results-count"><b>0</b> résultats</div>
            <select class="sort-select" id="sort-sel" onchange="applyFilters()">
            <option value="recent">Plus récent</option>
            <option value="price-asc">Prix croissant</option>
            <option value="price-desc">Prix décroissant</option>
          </select>
          </div>
          <div class="results-grid" id="results-grid"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- ════════════════════════════════════════
     PRODUCT DETAIL PAGE
════════════════════════════════════════ -->
  <div id="page-product" class="page">
    <div class="container">
      <div class="breadcrumb"><a onclick="showPage('home')">Accueil</a><span class="sep">›</span><a
          onclick="showPage('search')">Annonces</a><span class="sep">›</span><span id="det-breadcrumb">Article</span>
      </div>
      <div class="prod-detail-grid">
        <div class="prod-imgs">
          <div class="prod-main-img" id="det-main-img">📦</div>
          <div class="prod-thumbs" id="det-thumbs"></div>
        </div>
        <div class="prod-info-panel">
          <div class="prod-info-card">
            <div class="prod-detail-price" id="det-price">— FCFA</div>
            <div class="prod-detail-name" id="det-name">—</div>
            <div class="prod-detail-meta" id="det-meta"></div>
            <hr style="border:none;border-top:1px solid var(--border);margin:12px 0" />
            <div class="prod-detail-desc" id="det-desc">—</div>
          </div>
          <div class="prod-info-card">
            <div
              style="font-size:.78rem;font-weight:700;color:var(--muted);margin-bottom:10px;text-transform:uppercase;letter-spacing:.5px">
              Vendeur</div>
            <div class="seller-card" id="det-seller-card">
              <div class="seller-av" id="det-seller-av">?</div>
              <div>
                <div class="seller-name" id="det-seller-name">—</div>
                <div class="seller-badge">✅ Compte vérifié WhatsApp</div>
                <div class="seller-loc" id="det-seller-loc">📍 Bouaké</div>
              </div>
            </div>
          </div>
          <div class="prod-info-card">
            <button class="btn-wa-big" id="det-wa-btn" onclick="">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="#fff"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.127.557 4.123 1.529 5.855L.057 23.886l6.198-1.626A11.93 11.93 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.017-1.374l-.36-.214-3.727.977 1.002-3.651-.235-.374A9.818 9.818 0 012.182 12c0-5.42 4.398-9.818 9.818-9.818 5.42 0 9.818 4.398 9.818 9.818 0 5.42-4.398 9.818-9.818 9.818z"/></svg>
            Contacter le vendeur sur WhatsApp
          </button>
            <button class="btn-save" onclick="toggleFav()">❤️ Sauvegarder l'annonce</button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ════════════════════════════════════════
     DASHBOARD
════════════════════════════════════════ -->
  <div id="page-dashboard" class="page">
    <div class="container">
      <div class="dash-layout">
        <div class="dash-sidebar">
          <div style="padding:18px;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:10px">
            <div id="dash-av-lg"
              style="width:42px;height:42px;border-radius:50%;background:var(--gr);display:flex;align-items:center;justify-content:center;font-size:1.1rem;color:#fff;font-weight:700;overflow:hidden;flex-shrink:0">
            </div>
            <div>
              <div style="font-weight:700;font-size:.85rem" id="dash-name-lg">—</div>
              <div style="font-size:.7rem;color:var(--muted)" id="dash-email-sm">—</div>
            </div>
          </div>
          <div class="dash-menu-item active-menu" onclick="showDashTab('overview',this)">📊 Tableau de bord</div>
          <div class="dash-menu-item" onclick="showDashTab('myads',this)">📢 Mes annonces</div>
          <div class="dash-menu-item" onclick="showDashTab('publish',this)">➕ Publier une annonce</div>
          <div class="dash-menu-item" onclick="showDashTab('profile',this)">👤 Mon profil</div>
          <div class="dash-menu-item" onclick="showDashTab('favs',this)">❤️ Mes favoris</div>
          <div class="dash-menu-item" style="color:var(--red)" onclick="logout()">← Déconnexion</div>
        </div>
        <div class="dash-content">

          <!-- OVERVIEW -->
          <div id="tab-overview">
            <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.05rem;margin-bottom:14px">Bonjour,
              <span style="color:var(--gr)" id="dash-hello">—</span> 👋</div>
            <div class="dash-stats-row">
              <div class="ds-card">
                <div class="ds-val" style="color:var(--gr)" id="my-ads-count">0</div>
                <div class="ds-lbl">📢 Mes annonces</div>
              </div>
              <div class="ds-card">
                <div class="ds-val" style="color:var(--or)" id="my-views">0</div>
                <div class="ds-lbl">👁️ Vues totales</div>
              </div>
              <div class="ds-card">
                <div class="ds-val" style="color:var(--wa)" id="my-contacts">0</div>
                <div class="ds-lbl">💬 Contacts WA</div>
              </div>
              <div class="ds-card">
                <div class="ds-val" style="color:var(--blue)" id="my-favs-count">0</div>
                <div class="ds-lbl">❤️ Favoris</div>
              </div>
            </div>
            <div style="background:#fff;border-radius:12px;padding:18px;box-shadow:var(--shadow)">
              <div style="font-weight:700;font-size:.88rem;margin-bottom:10px">🏅 Votre profil</div>
              <div id="profile-info-block" style="font-size:.82rem;color:var(--muted);line-height:1.8"></div>
            </div>
          </div>

          <!-- MY ADS -->
          <div id="tab-myads" style="display:none">
            <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:14px">
              <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.05rem">Mes annonces</div>
              <button class="m-btn m-btn-primary" style="width:auto;padding:9px 18px;font-size:.82rem" onclick="showDashTab('publish',null)">+ Nouvelle annonce</button>
            </div>
            <div class="dash-ads-grid" id="my-ads-grid">
              <div class="empty-state" style="grid-column:1/-1">
                <div class="empty-ico">📭</div>
                <div class="empty-title">Aucune annonce</div>
                <div class="empty-sub">Publiez votre première annonce !</div>
              </div>
            </div>
          </div>

          <!-- PUBLISH -->
          <div id="tab-publish" style="display:none">
            <div class="publish-form">
              <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.05rem;margin-bottom:18px">➕ Publier
                une annonce</div>
              <div class="pub-steps">
                <div class="pub-step ps-active" id="pstep1">
                  <div class="ps-circle">1</div>
                  <div class="ps-label">Photos</div>
                </div>
                <div class="pub-step" id="pstep2">
                  <div class="ps-circle">2</div>
                  <div class="ps-label">Infos</div>
                </div>
                <div class="pub-step" id="pstep3">
                  <div class="ps-circle">3</div>
                  <div class="ps-label">Contact</div>
                </div>
                <div class="pub-step" id="pstep4">
                  <div class="ps-circle">4</div>
                  <div class="ps-label">Publier</div>
                </div>
              </div>

              <div class="pf-section pf-active" id="pf1">
                <div class="pf-title">📸 Photos de l'article</div>
                <div class="pf-sub">Ajoutez jusqu'à 6 photos (la 1ère = photo principale)</div>
                <div class="photo-grid-upload" id="pub-photo-grid"></div>
                <div class="pf-nav">
                  <button class="btn m-btn-outline" onclick="showPage('dashboard')">Annuler</button><button class="btn m-btn-primary" onclick="pfNext(2)">Suivant →</button>
                </div>
              </div>

              <div class="pf-section" id="pf2">
                <div class="pf-title">📝 Détails de l'article</div>
                <div class="pf-sub">Décrivez ce que vous vendez avec précision.</div>
                <div class="fl">
                  <div class="fg"><label>Catégorie <span class="req-star">*</span></label>
                    <select id="pf-cat"><option value="">-- Choisir --</option><option value="phones">📱 Téléphones</option><option value="info">🖥️ Informatique</option><option value="mode">👗 Mode</option><option value="motos">🛵 Motos</option><option value="voitures">🚗 Voitures</option><option value="immo">🏠 Immobilier</option><option value="meubles">🛋️ Meubles</option><option value="sport">⚽ Sport</option><option value="alim">🍎 Alimentation</option><option value="autres">💼 Autres</option></select>
                  </div>
                  <div class="fg"><label>État</label>
                    <select id="pf-etat"><option value="bon">Bon état</option><option value="neuf">Neuf</option><option value="usage">Usagé</option></select>
                  </div>
                </div>
                <div class="fg"><label>Titre de l'annonce <span class="req-star">*</span></label><input type="text" id="pf-title" placeholder="Ex: iPhone 13 Pro Max 256Go — Parfait état" maxlength="80"/>
                </div>
                <div class="fg">
                  <label>Description</label><textarea id="pf-desc" placeholder="Décrivez l'état, les caractéristiques, les raisons de la vente..."></textarea>
                </div>
                <div class="fl">
                  <div class="fg"><label>Prix (FCFA) <span class="req-star">*</span></label>
                    <div class="price-input-wrap">
                      <div class="pcur">FCFA</div><input type="number" id="pf-price" class="pinp" placeholder="0" min="0"/>
                    </div>
                  </div>
                  <div class="fg"><label>Quartier</label><input type="text" id="pf-lieu" placeholder="Ex: Koko, Commerce..."/>
                  </div>
                </div>
                <div class="pf-nav">
                  <button class="btn m-btn-outline" onclick="pfBack(1)">← Retour</button><button class="btn m-btn-primary" onclick="pfNext(3)">Suivant →</button>
                </div>
              </div>

              <div class="pf-section" id="pf3">
                <div class="pf-title">📲 Contact WhatsApp</div>
                <div class="pf-sub">Les acheteurs vous contacteront directement sur WhatsApp.</div>
                <div class="fg"><label>Numéro WhatsApp</label>
                  <div class="wa-input-group">
                    <div class="wa-pref"><svg width="13" height="13" viewBox="0 0 24 24" fill="#25D366">
                        <path
                          d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z" />
                        <path
                          d="M12 0C5.373 0 0 5.373 0 12c0 2.127.557 4.123 1.529 5.855L.057 23.886l6.198-1.626A11.93 11.93 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.017-1.374l-.36-.214-3.727.977 1.002-3.651-.235-.374A9.818 9.818 0 012.182 12c0-5.42 4.398-9.818 9.818-9.818 5.42 0 9.818 4.398 9.818 9.818 0 5.42-4.398 9.818-9.818 9.818z" />
                      </svg>+225</div><input class="wa-suf" type="tel" id="pf-wa" placeholder="07 00 00 00 00" maxlength="14"/>
                  </div>
                </div>
                <div class="fg"><label>Nom affiché</label><input type="text" id="pf-seller-name" placeholder="Votre prénom ou nom de boutique"/>
                </div>
                <div class="pf-nav">
                  <button class="btn m-btn-outline" onclick="pfBack(2)">← Retour</button><button class="btn m-btn-primary" onclick="pfNext(4)">Aperçu →</button>
                </div>
              </div>

              <div class="pf-section" id="pf4">
                <div class="pf-title">👁️ Aperçu avant publication</div>
                <div class="pf-sub">Vérifiez votre annonce avant de la publier.</div>
                <div
                  style="background:var(--light);border:1px solid var(--border);border-radius:11px;overflow:hidden;margin-bottom:16px">
                  <div
                    style="height:160px;background:var(--border);display:flex;align-items:center;justify-content:center;font-size:4rem;position:relative;overflow:hidden"
                    id="pf-prev-img">📦</div>
                  <div style="padding:14px">
                    <div
                      style="font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:var(--or);margin-bottom:4px"
                      id="pf-prev-price">—</div>
                    <div style="font-weight:700;font-size:.9rem;margin-bottom:5px" id="pf-prev-title">—</div>
                    <div style="font-size:.74rem;color:var(--muted);margin-bottom:8px" id="pf-prev-meta">—</div>
                    <div style="font-size:.8rem;color:var(--text);line-height:1.5;margin-bottom:10px" id="pf-prev-desc">
                      —</div>
                    <div
                      style="background:#f0fff8;border:1px solid rgba(0,168,107,.2);border-radius:8px;padding:10px;display:flex;align-items:center;gap:8px">
                      <div style="font-size:1.1rem">💬</div>
                      <div>
                        <div style="font-size:.78rem;color:var(--wa);font-weight:600">WhatsApp</div>
                        <div style="font-size:.72rem;color:var(--muted)" id="pf-prev-wa">+225 —</div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="pf-nav">
                  <button class="btn m-btn-outline" onclick="pfBack(3)">← Modifier</button>
                  <button class="btn m-btn-primary" style="flex:2;background:var(--or)" onclick="publishAd()">🚀 Publier maintenant !</button>
                </div>
              </div>
            </div>
          </div>

          <!-- PROFILE -->
          <div id="tab-profile" style="display:none">
            <div style="background:#fff;border-radius:12px;padding:22px;box-shadow:var(--shadow)">
              <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.05rem;margin-bottom:18px">👤 Mon
                profil</div>
              <div style="display:flex;align-items:center;gap:16px;margin-bottom:22px">
                <div id="profile-av-big"
                  style="width:64px;height:64px;border-radius:50%;background:var(--gr);display:flex;align-items:center;justify-content:center;font-size:1.6rem;color:#fff;font-weight:700;overflow:hidden;border:3px solid var(--gr);flex-shrink:0">
                </div>
                <div>
                  <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1rem" id="profile-name-big">—
                  </div>
                  <div style="font-size:.78rem;color:var(--wa);margin-top:3px" id="profile-phone-big">—</div>
                  <div style="font-size:.72rem;color:var(--muted);margin-top:1px" id="profile-email-big">—</div>
                </div>
              </div>
              <div id="profile-details" style="font-size:.84rem;line-height:2;color:var(--text)"></div>
            </div>
          </div>

          <!-- FAVORITES -->
          <div id="tab-favs" style="display:none">
            <div style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.05rem;margin-bottom:14px">❤️ Mes
              favoris</div>
            <div class="results-grid" id="favs-grid">
              <div class="empty-state" style="grid-column:1/-1">
                <div class="empty-ico">💔</div>
                <div class="empty-title">Aucun favori</div>
                <div class="empty-sub">Cliquez sur ❤️ sur une annonce pour la sauvegarder</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ════════════════════════════════════════
     OVERLAY — SIGNUP (4 steps)
════════════════════════════════════════ -->
  <div class="overlay" id="ov-signup">
    <div class="modal">
      <button class="modal-x" onclick="closeOverlay('signup')">✕</button>

      <!-- S1: base -->
      <div id="su-s1">
        <div class="modal-logo">JFK SERVICE BOUAKÉ</div>
        <div class="modal-title">Créer un compte</div>
        <div class="modal-sub">Rejoignez la communauté JFK à Bouaké 🇨🇮</div>
        <button class="g-btn" onclick="googleAuth()"><svg viewBox="0 0 24 24"><path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/><path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/><path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l3.66-2.84z"/><path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84z"/></svg>Continuer avec Google</button>
        <div class="div-or">ou avec email</div>
        <div class="mfg"><label>Prénom &amp; Nom <span class="req-star">*</span></label><input type="text" id="su-nm" placeholder="Ex: Koné Amadou"/>
          <div class="err-row" id="e-su-nm">⚠️ Entrez votre nom complet</div>
        </div>
        <div class="mfg"><label>Gmail <span class="req-star">*</span></label><input type="email" id="su-em" placeholder="exemple@gmail.com"/>
          <div class="err-row" id="e-su-em">⚠️ Email invalide</div>
        </div>
        <div class="mfg"><label>Mot de passe <span class="req-star">*</span></label>
          <div class="pw-wrap">
            <input type="password" id="su-pw" placeholder="Minimum 6 caractères"/><button class="pw-eye" onclick="tpw('su-pw',this)">👁</button>
          </div>
          <div class="err-row" id="e-su-pw">⚠️ Minimum 6 caractères</div>
        </div>
        <div class="mfg"><label>Confirmer mot de passe <span class="req-star">*</span></label>
          <div class="pw-wrap">
            <input type="password" id="su-pw2" placeholder="Répétez le mot de passe"/><button class="pw-eye" onclick="tpw('su-pw2',this)">👁</button>
          </div>
          <div class="err-row" id="e-su-pw2">⚠️ Mots de passe différents</div>
        </div>
        <button class="m-btn m-btn-primary" onclick="suS1()">Continuer →</button>
        <div class="modal-switch">Déjà inscrit ? <a onclick="switchOv('signup','login')">Se connecter</a></div>
      </div>

      <!-- S2: profil -->
      <div id="su-s2" style="display:none">
        <div class="modal-logo">JFK SERVICE BOUAKÉ</div>
        <div class="modal-title">Votre profil</div>
        <div class="modal-sub">Ajoutez votre photo et votre numéro WhatsApp.</div>
        <div class="av-upload-row">
          <div class="av-ring" id="su-av-ring" onclick="document.getElementById('su-av-inp').click()">
            <div style="font-size:1.8rem;opacity:.35">👤</div>
            <div class="av-edit-ov">📷<br>Changer</div>
            <input type="file" id="su-av-inp" accept="image/*" style="display:none" onchange="suSetAvatar(this)"/>
          </div>
          <div class="av-hint">Photo de profil (recommandée)</div>
        </div>
        <div class="mfg">
          <label>Numéro WhatsApp <span class="req-star">* Obligatoire</span></label>
          <div class="ph-wrap">
            <div class="ph-pfx"><svg width="12" height="12" viewBox="0 0 24 24" fill="#25D366">
                <path
                  d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z" />
                <path
                  d="M12 0C5.373 0 0 5.373 0 12c0 2.127.557 4.123 1.529 5.855L.057 23.886l6.198-1.626A11.93 11.93 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.017-1.374l-.36-.214-3.727.977 1.002-3.651-.235-.374A9.818 9.818 0 012.182 12c0-5.42 4.398-9.818 9.818-9.818 5.42 0 9.818 4.398 9.818 9.818 0 5.42-4.398 9.818-9.818 9.818z" />
              </svg>+225</div><input type="tel" id="su-ph" class="ph-sfx" placeholder="07 00 00 00 00" maxlength="14"/>
          </div>
          <div class="err-row" id="e-su-ph">⚠️ Entrez votre numéro WhatsApp</div>
          <div class="hint" style="font-size:.7rem;color:var(--muted);margin-top:4px">📲 Un code de vérification sera
            envoyé sur WhatsApp</div>
        </div>
        <div class="mfg"><label>Quartier à Bouaké</label><input type="text" id="su-qrt" placeholder="Ex: Koko, Air France, Bromakoté..."/>
        </div>
        <div style="display:flex;gap:9px">
          <button class="m-btn m-btn-outline" onclick="suGoS1()">← Retour</button>
          <button class="m-btn m-btn-wa" onclick="suSendOtp()" style="flex:2">📲 Envoyer le code WhatsApp</button>
        </div>
      </div>

      <!-- S3: OTP -->
      <div id="su-s3" style="display:none">
        <div class="modal-logo">JFK SERVICE BOUAKÉ</div>
        <div class="modal-title">Vérification</div>
        <div class="modal-sub">Code à 4 chiffres envoyé sur WhatsApp.</div>
        <div class="otp-box">💬 Numéro : <span class="otp-num" id="su-otp-ph">+225 —</span></div>
        <div class="otp-sim">🔔 <b>Mode démo :</b> Dans l'app réelle, le code arrive par WhatsApp.<br>Code de test :
          <b id="su-otp-show" style="letter-spacing:4px;font-size:1rem">—</b></div>
        <div class="otp-digits">
          <input class="otp-d" id="od0" type="tel" maxlength="1" oninput="oi(0,this)" onkeydown="okd(0,event)"/>
          <input class="otp-d" id="od1" type="tel" maxlength="1" oninput="oi(1,this)" onkeydown="okd(1,event)"/>
          <input class="otp-d" id="od2" type="tel" maxlength="1" oninput="oi(2,this)" onkeydown="okd(2,event)"/>
          <input class="otp-d" id="od3" type="tel" maxlength="1" oninput="oi(3,this)" onkeydown="okd(3,event)"/>
        </div>
        <div class="otp-timer" id="otp-tmr-txt">Code valide <b id="otp-tmr-cnt">120</b>s</div>
        <div class="otp-resend" id="otp-resend-lnk" onclick="suResendOtp()">↺ Renvoyer le code</div>
        <button class="m-btn m-btn-primary" style="margin-top:12px" onclick="suVerify()">✅ Vérifier le code</button>
        <button class="m-btn m-btn-outline" onclick="suGoS2()">← Modifier le numéro</button>
      </div>

      <!-- S4: success -->
      <div id="su-s4" style="display:none">
        <div class="success-block">
          <div class="sb-ico">🎉</div>
          <div class="sb-title">Compte créé !</div>
          <div class="sb-sub">WhatsApp vérifié. Bienvenue sur JFK Service Bouaké !</div>
          <div class="profile-mini">
            <div class="pm-av" id="su-pm-av">👤</div>
            <div>
              <div class="pm-name" id="su-pm-nm">—</div>
              <div class="pm-phone" id="su-pm-ph">—</div>
              <div class="pm-email" id="su-pm-em">—</div>
            </div>
          </div>
          <button class="m-btn m-btn-primary" onclick="suFinish()">Accéder à mon espace →</button>
        </div>
      </div>
    </div>
  </div>

  <!-- ════ LOGIN OVERLAY ════ -->
  <div class="overlay" id="ov-login">
    <div class="modal">
      <button class="modal-x" onclick="closeOverlay('login')">✕</button>
      <div class="modal-logo">JFK SERVICE BOUAKÉ</div>
      <div class="modal-title">Connexion</div>
      <div class="modal-sub">Content de vous revoir 👋</div>
      <button class="g-btn" onclick="googleAuth()"><svg viewBox="0 0 24 24"><path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/><path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/><path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l3.66-2.84z"/><path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84z"/></svg>Continuer avec Google</button>
      <div class="div-or">ou email</div>
      <div class="mfg"><label>Gmail</label><input type="email" id="li-em" placeholder="exemple@gmail.com" oninput="clearLi()"/>
        <div class="err-row" id="e-li-em">⚠️ Aucun compte avec cet email</div>
      </div>
      <div class="mfg"><label>Mot de passe</label>
        <div class="pw-wrap">
          <input type="password" id="li-pw" placeholder="Votre mot de passe" oninput="clearLi()"/><button class="pw-eye" onclick="tpw('li-pw',this)">👁</button>
        </div>
        <div class="err-row" id="e-li-pw">🔐 Mot de passe incorrect</div><a class="forgot-a"
          onclick="switchOv('login','forgot')">Mot de passe oublié ?</a>
      </div>
      <div class="err-row" id="e-li-global" style="margin-bottom:11px">❌
        <span id="e-li-txt">Email ou mot de passe incorrect</span></div>
      <button class="m-btn m-btn-primary" onclick="doLogin()">Se connecter</button>
      <div class="modal-switch">Pas de compte ? <a onclick="switchOv('login','signup')">S'inscrire gratuitement</a>
      </div>
    </div>
  </div>

  <!-- ════ FORGOT OVERLAY ════ -->
  <div class="overlay" id="ov-forgot">
    <div class="modal">
      <button class="modal-x" onclick="closeOverlay('forgot')">✕</button>
      <div class="modal-logo">JFK SERVICE BOUAKÉ</div>
      <div class="modal-title">Mot de passe oublié ?</div>
      <div class="modal-sub">Entrez votre Gmail pour recevoir un lien de réinitialisation.</div>
      <div id="fo-form">
        <div class="mfg"><label>Gmail</label><input type="email" id="fo-em" placeholder="exemple@gmail.com"/>
          <div class="err-row" id="e-fo-em">⚠️ Email invalide</div>
        </div>
        <button class="m-btn m-btn-primary" onclick="doForgot()">Envoyer le lien</button>
        <div class="modal-switch"><a onclick="switchOv('forgot','login')">← Retour à la connexion</a></div>
      </div>
      <div id="fo-ok" style="display:none">
        <div class="success-block">
          <div class="sb-ico">📧</div>
          <div class="sb-title">Email envoyé !</div>
          <div class="sb-sub">Vérifiez votre boîte Gmail pour réinitialiser votre mot de passe.</div>
          <button class="m-btn m-btn-outline" style="margin-top:14px" onclick="switchOv('forgot','login')">Retour connexion</button>
        </div>
      </div>
    </div>
  </div>

  <div class="toast" id="toast"></div>

  <script>
    /* ═══════════════ STATE ═══════════════ */
const STORE_KEY = 'jfk_data_v1';
let state = {
  users: [],
  ads: [],
  favs: [],
  currentUser: null
};

/* ═══ PERSIST TO localStorage ═══ */
function saveState() {
  try { localStorage.setItem(STORE_KEY, JSON.stringify(state)); } catch(e){}
}
function loadState() {
  try {
    const s = localStorage.getItem(STORE_KEY);
    if (s) { const p = JSON.parse(s); Object.assign(state, p); }
  } catch(e){}
}

/* ═══ INIT ═══ */
loadState();
// Supprimer les anciennes annonces de démo si elles existent dans le cache local
const demoIds = ['d1','d2','d3','d4','d5','d6'];
if (state.ads.some(a => demoIds.includes(a.id))) {
  state.ads = state.ads.filter(a => !demoIds.includes(a.id));
  saveState();
}
// Page vide au départ — seules les vraies annonces publiées apparaissent

/* ═══ BANNER CAROUSEL ═══ */
let bannerIdx = 0;
function goBanner(n) {
  bannerIdx = n;
  document.getElementById('banner-slides').style.transform = `translateX(-${n*100}%)`;
  document.querySelectorAll('.banner-dot').forEach((d,i) => d.classList.toggle('active', i===n));
}
function nextBanner() { goBanner((bannerIdx+1)%3); }
function prevBanner() { goBanner((bannerIdx+2)%3); }
setInterval(nextBanner, 4500);

/* ═══ PAGES ═══ */
function showPage(name) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + name).classList.add('active');
  window.scrollTo(0, 0);
  if (name === 'home') { renderHomepage(); }
  if (name === 'dashboard') { if (!state.currentUser) { openOverlay('login'); return; } renderDashboard(); }
  if (name === 'search') { applyFilters(); }
}

/* ═══ TOAST ═══ */
function toast(msg, type='ok', dur=3200) {
  const el = document.getElementById('toast');
  el.textContent = msg;
  el.className = 'toast t-' + type;
  el.classList.add('show');
  setTimeout(() => el.classList.remove('show'), dur);
}

/* ═══ OVERLAYS ═══ */
function openOverlay(name) { document.getElementById('ov-' + name).classList.add('open'); }
function closeOverlay(name) {
  document.getElementById('ov-' + name).classList.remove('open');
  if (name === 'signup') resetSu();
}
function switchOv(a, b) { closeOverlay(a); openOverlay(b); }
document.querySelectorAll('.overlay').forEach(o => o.addEventListener('click', e => { if(e.target===o) o.classList.remove('open'); }));

/* ═══ TOGGLE PASSWORD ═══ */
function tpw(id, btn) {
  const el = document.getElementById(id);
  el.type = el.type === 'password' ? 'text' : 'password';
  btn.textContent = el.type === 'password' ? '👁' : '🙈';
}

/* ═══ ERR HELPERS ═══ */
function showE(eid, iid) { const e=document.getElementById(eid); if(e) e.classList.add('show'); const i=document.getElementById(iid); if(i) i.classList.add('ef'); }
function clearAllE() { document.querySelectorAll('.err-row').forEach(e=>e.classList.remove('show')); document.querySelectorAll('.mfg input,.mfg select').forEach(i=>i.classList.remove('ef')); }
function clearLi() { clearAllE(); }

/* ═══════════════ SIGNUP ═══════════════ */
let suData = {}, suOtp = null, suOtpTimer = null, suAvUrl = null;

function resetSu() {
  ['su-s1','su-s2','su-s3','su-s4'].forEach((id,i) => document.getElementById(id).style.display = i===0 ? 'block' : 'none');
  clearInterval(suOtpTimer); suOtpTimer = null; suAvUrl = null; suData = {};
  ['su-nm','su-em','su-pw','su-pw2','su-ph','su-qrt'].forEach(id => { const e=document.getElementById(id); if(e) e.value=''; });
  const r = document.getElementById('su-av-ring');
  r.innerHTML = '<div style="font-size:1.8rem;opacity:.35">👤</div><div class="av-edit-ov">📷<br>Changer</div><input type="file" id="su-av-inp" accept="image/*" style="display:none" onchange="suSetAvatar(this)"/>';
  clearAllE();
}

function suSetAvatar(inp) {
  if (!inp.files[0]) return;
  const r = new FileReader();
  r.onload = e => {
    suAvUrl = e.target.result;
    const ring = document.getElementById('su-av-ring');
    ring.innerHTML = `<img src="${suAvUrl}" alt="av"/><div class="av-edit-ov">📷<br>Changer</div><input type="file" id="su-av-inp" accept="image/*" style="display:none" onchange="suSetAvatar(this)"/>`;
    ring.onclick = () => document.getElementById('su-av-inp').click();
    toast('✅ Photo de profil ajoutée !');
  };
  r.readAsDataURL(inp.files[0]);
}

function suS1() {
  clearAllE();
  const nm=document.getElementById('su-nm').value.trim();
  const em=document.getElementById('su-em').value.trim();
  const pw=document.getElementById('su-pw').value;
  const pw2=document.getElementById('su-pw2').value;
  let ok=true;
  if(!nm){showE('e-su-nm','su-nm');ok=false;}
  if(!em||!em.includes('@')){showE('e-su-em','su-em');ok=false;}
  if(pw.length<6){showE('e-su-pw','su-pw');ok=false;}
  if(pw!==pw2){showE('e-su-pw2','su-pw2');ok=false;}
  if(!ok) return;
  suData = { name:nm, email:em, pass:pw };
  document.getElementById('su-s1').style.display='none';
  document.getElementById('su-s2').style.display='block';
}
function suGoS1() { document.getElementById('su-s2').style.display='none'; document.getElementById('su-s1').style.display='block'; }
function suGoS2() { clearInterval(suOtpTimer); document.getElementById('su-s3').style.display='none'; document.getElementById('su-s2').style.display='block'; }

function suSendOtp() {
  clearAllE();
  const ph = document.getElementById('su-ph').value.replace(/\s/g,'');
  if (!ph || ph.length < 8) { showE('e-su-ph','su-ph'); return; }
  suData.phone = ph;
  suData.quartier = document.getElementById('su-qrt').value.trim();
  suData.avatarUrl = suAvUrl;
  suOtp = String(Math.floor(1000 + Math.random()*9000));
  document.getElementById('su-s2').style.display='none';
  document.getElementById('su-s3').style.display='block';
  document.getElementById('su-otp-ph').textContent = '+225 '+ph;
  document.getElementById('su-otp-show').textContent = suOtp;
  [0,1,2,3].forEach(i=>{const el=document.getElementById('od'+i);el.value='';el.classList.remove('ok','bad');});
  document.getElementById('od0').focus();
  startOtpTimer();
  toast('📲 Code envoyé sur WhatsApp +225 '+ph, 'wa', 4000);
}

function startOtpTimer() {
  clearInterval(suOtpTimer); suOtpTimer = null;
  let s = 120;
  document.getElementById('otp-tmr-cnt').textContent = s;
  document.getElementById('otp-tmr-txt').style.display = 'block';
  document.getElementById('otp-resend-lnk').style.display = 'none';
  suOtpTimer = setInterval(()=>{
    s--;
    document.getElementById('otp-tmr-cnt').textContent = s;
    if (s<=0) {
      clearInterval(suOtpTimer);
      document.getElementById('otp-tmr-txt').style.display='none';
      document.getElementById('otp-resend-lnk').style.display='block';
    }
  }, 1000);
}
function suResendOtp() {
  suOtp = String(Math.floor(1000+Math.random()*9000));
  document.getElementById('su-otp-show').textContent = suOtp;
  [0,1,2,3].forEach(i=>{const el=document.getElementById('od'+i);el.value='';el.classList.remove('ok','bad');});
  document.getElementById('od0').focus();
  startOtpTimer();
  toast('📲 Nouveau code envoyé !','wa');
}

function oi(i,el){
  const v=el.value.replace(/\D/g,'');el.value=v.slice(-1);
  if(v){el.classList.add('ok');if(i<3)document.getElementById('od'+(i+1)).focus();}
  else el.classList.remove('ok');
}
function okd(i,e){if(e.key==='Backspace'&&!document.getElementById('od'+i).value&&i>0)document.getElementById('od'+(i-1)).focus();}

function suVerify() {
  const entered = [0,1,2,3].map(i=>document.getElementById('od'+i).value).join('');
  if (entered.length < 4) { toast('⚠️ Entrez les 4 chiffres','err'); return; }
  if (entered !== suOtp) {
    [0,1,2,3].forEach(i=>{const el=document.getElementById('od'+i);el.classList.add('bad');el.classList.remove('ok');});
    toast('❌ Code incorrect ! Réessayez.','err');
    setTimeout(()=>{[0,1,2,3].forEach(i=>{const el=document.getElementById('od'+i);el.classList.remove('bad');el.value='';});document.getElementById('od0').focus();},900);
    return;
  }
  clearInterval(suOtpTimer);
  const u = { id:'u'+Date.now(), ...suData, createdAt: Date.now() };
  state.users.push(u);
  saveState();
  document.getElementById('su-s3').style.display='none';
  document.getElementById('su-s4').style.display='block';
  document.getElementById('su-pm-nm').textContent = u.name;
  document.getElementById('su-pm-ph').textContent = '📲 +225 '+u.phone;
  document.getElementById('su-pm-em').textContent = '✉️ '+u.email;
  const pmAv = document.getElementById('su-pm-av');
  if (u.avatarUrl) pmAv.innerHTML = `<img src="${u.avatarUrl}" alt="av"/>`;
  else { pmAv.textContent = u.name.charAt(0).toUpperCase(); }
  updateStatsBand();
}

function suFinish() {
  const u = state.users[state.users.length-1];
  state.currentUser = u;
  saveState();
  closeOverlay('signup');
  resetSu();
  updateNav();
  showPage('dashboard');
  toast('🎉 Bienvenue '+u.name+' !','wa',3500);
}

/* ═══════════════ LOGIN ═══════════════ */
function doLogin() {
  clearAllE();
  const em = document.getElementById('li-em').value.trim();
  const pw = document.getElementById('li-pw').value;
  if (!em||!em.includes('@')) { showE('e-li-em','li-em'); return; }
  if (!pw) { showE('e-li-pw','li-pw'); return; }
  const found = state.users.find(u => u.email.toLowerCase()===em.toLowerCase());
  if (!found) {
    document.getElementById('e-li-txt').textContent = 'Aucun compte trouvé avec cet email. Vérifiez ou créez un compte.';
    document.getElementById('e-li-global').classList.add('show');
    document.getElementById('li-em').classList.add('ef');
    toast('❌ Gmail introuvable','err'); return;
  }
  if (found.pass !== pw) {
    document.getElementById('e-li-txt').textContent = 'Mot de passe incorrect. Réessayez ou utilisez "Mot de passe oublié".';
    document.getElementById('e-li-global').classList.add('show');
    document.getElementById('li-pw').classList.add('ef');
    toast('🔐 Mot de passe incorrect','err'); return;
  }
  state.currentUser = found;
  saveState();
  closeOverlay('login');
  document.getElementById('li-em').value=''; document.getElementById('li-pw').value='';
  updateNav();
  showPage('dashboard');
  toast('✅ Connexion réussie ! Bonjour '+found.name);
}

/* Google */
function googleAuth() {
  const g = {id:'google-1',name:'Google Utilisateur',email:'user.google@gmail.com',pass:'google',phone:'0700000000',quartier:'Bouaké',avatarUrl:null,createdAt:Date.now()};
  if (!state.users.find(u=>u.email===g.email)) { state.users.push(g); saveState(); }
  state.currentUser = state.users.find(u=>u.email===g.email);
  saveState();
  closeOverlay('login'); closeOverlay('signup');
  updateNav(); showPage('dashboard');
  toast('✅ Connecté via Google !','wa');
}

/* Forgot */
function doForgot() {
  clearAllE();
  const em = document.getElementById('fo-em').value.trim();
  if (!em||!em.includes('@')) { showE('e-fo-em','fo-em'); return; }
  document.getElementById('fo-form').style.display='none';
  document.getElementById('fo-ok').style.display='block';
}

/* Logout */
function logout() {
  state.currentUser = null;
  saveState();
  updateNav();
  showPage('home');
  toast('👋 Déconnexion réussie');
}

/* ═══════════════ UPDATE NAV ═══════════════ */
function updateNav() {
  const acts = document.getElementById('nav-actions');
  const tb = document.getElementById('tb-user-info');
  if (state.currentUser) {
    const u = state.currentUser;
    const avHtml = u.avatarUrl
      ? `<div class="nav-av"><img src="${u.avatarUrl}" alt="av"/></div>`
      : `<div class="nav-av">${u.name.charAt(0).toUpperCase()}</div>`;
    acts.innerHTML = `
      <button class="nav-icon-btn" title="Favoris" onclick="showPage('dashboard')">❤️<span class="nav-badge" id="fav-count">${state.favs.length}</span></button>
      <div class="nav-avatar-btn" onclick="showPage('dashboard')">${avHtml}<span>${u.name.split(' ')[0]}</span></div>
      <button class="nav-btn" onclick="showPage('dashboard')" style="background:rgba(255,255,255,.15)">📢 Vendre</button>`;
    tb.textContent = '👤 ' + u.name + ' — Bienvenue !';
  } else {
    acts.innerHTML = `
      <button class="nav-icon-btn" title="Favoris">❤️<span class="nav-badge" id="fav-count">${state.favs.length}</span></button>
      <button class="nav-btn" onclick="openOverlay('login')">Se connecter</button>
      <button class="nav-btn-solid" onclick="openOverlay('signup')">S'inscrire</button>`;
    tb.textContent = '👋 Bienvenue sur JFK Service';
  }
}

/* ═══════════════ RENDER CARDS ═══════════════ */
function renderCard(ad, compact=false) {
  const price = Number(ad.price).toLocaleString('fr-FR');
  const badgeHtml = ad.badge ? `<div class="prod-badge ${ad.badge==='NEW'?'new':ad.badge==='HOT'?'hot':''}">${ad.badge}</div>` : '';
  const imgHtml = ad.img ? `<img src="${ad.img}" alt="${ad.title}"/>` : ad.emoji||'📦';
  return `
  <div class="prod-card" onclick="openProduct('${ad.id}')">
    <div class="prod-img">${imgHtml}${badgeHtml}<button class="prod-fav" onclick="toggleFavItem('${ad.id}',event)">${state.favs.includes(ad.id)?'❤️':'🤍'}</button></div>
    <div class="prod-body">
      <div class="prod-name">${ad.title}</div>
      <div class="prod-price">${price} FCFA</div>
      <div class="prod-loc">📍 ${ad.lieu||'Bouaké'}</div>
      <div class="prod-seller">✅ ${ad.seller?.name||'Vendeur'}</div>
      ${!compact?`<button class="prod-wa-btn" onclick="waContact('${ad.id}',event)">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="#fff"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.127.557 4.123 1.529 5.855L.057 23.886l6.198-1.626A11.93 11.93 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.818a9.818 9.818 0 01-5.017-1.374l-.36-.214-3.727.977 1.002-3.651-.235-.374A9.818 9.818 0 012.182 12c0-5.42 4.398-9.818 9.818-9.818 5.42 0 9.818 4.398 9.818 9.818 0 5.42-4.398 9.818-9.818 9.818z"/></svg>
        WhatsApp</button>`:'' }
    </div>
  </div>`;
}

/* ═══════════════ HOMEPAGE ═══════════════ */
function renderHomepage() {
  const grid = document.getElementById('recent-grid');
  if (state.ads.length === 0) {
    grid.innerHTML = `<div class="empty-state" style="grid-column:1/-1;padding:60px 20px">
      <div class="empty-ico">🏪</div>
      <div class="empty-title" style="font-size:1.1rem">Aucune annonce pour l'instant</div>
      <div class="empty-sub" style="max-width:360px;margin:8px auto 0">
        Le marché est prêt ! Les annonces apparaîtront ici dès que des vendeurs commenceront à publier.<br><br>
        <b>Soyez le premier à publier !</b>
      </div>
      <div style="display:flex;gap:10px;justify-content:center;margin-top:20px;flex-wrap:wrap">
        <button class="m-btn m-btn-primary" style="width:auto;padding:11px 24px;font-size:.88rem" onclick="openOverlay('signup')">✍️ Créer un compte</button>
        <button class="m-btn m-btn-outline" style="width:auto;padding:11px 24px;font-size:.88rem;border:1.5px solid var(--border2)" onclick="openOverlay('login')">Se connecter</button>
      </div>
    </div>`;
  } else {
    grid.innerHTML = state.ads.slice().reverse().slice(0,6).map(a=>renderCard(a)).join('');
  }
  // Category counts
  const cats = ['phones','mode','motos','voitures','immo','meubles','info','sport'];
  cats.forEach(c => {
    const el = document.getElementById('cnt-'+c);
    if (el) el.textContent = state.ads.filter(a=>a.cat===c).length + ' annonces';
  });
  updateStatsBand();
}

function updateStatsBand() {
  const su = document.getElementById('stat-users');
  const sa = document.getElementById('stat-ads');
  if(su) su.textContent = state.users.length.toLocaleString('fr-FR');
  if(sa) sa.textContent = state.ads.length.toLocaleString('fr-FR');
}

/* ═══════════════ SEARCH / FILTER ═══════════════ */
let currentCat = 'all', currentSearch = '';

function filterCat(cat, btn) {
  currentCat = cat;
  document.querySelectorAll('.cat-pill').forEach(p=>p.classList.remove('active'));
  if (btn) btn.classList.add('active');
  showPage('search');
  applyFilters();
}

function doSearch() {
  currentSearch = document.getElementById('main-search').value.trim().toLowerCase();
  showPage('search');
  applyFilters();
}
function searchOnEnter(e) { if(e.key==='Enter') doSearch(); }

function updatePriceLabel(el) {
  document.getElementById('price-label').textContent = Number(el.value).toLocaleString('fr-FR') + ' FCFA';
}

function applyFilters() {
  let ads = [...state.ads];
  // cat filter
  if (currentCat && currentCat !== 'all') ads = ads.filter(a=>a.cat===currentCat);
  // search
  const q = document.getElementById('main-search').value.trim().toLowerCase();
  if (q) ads = ads.filter(a => a.title.toLowerCase().includes(q) || (a.desc||'').toLowerCase().includes(q) || (a.lieu||'').toLowerCase().includes(q));
  // price
  const maxP = document.getElementById('price-range')?.value || 5000000;
  ads = ads.filter(a => a.price <= Number(maxP));
  // sort
  const sort = document.getElementById('sort-sel')?.value || 'recent';
  if (sort==='price-asc') ads.sort((a,b)=>a.price-b.price);
  else if (sort==='price-desc') ads.sort((a,b)=>b.price-a.price);
  else ads.sort((a,b)=>b.createdAt-a.createdAt);

  const grid = document.getElementById('results-grid');
  const count = document.getElementById('results-count');
  const breadcrumb = document.getElementById('srch-breadcrumb');

  const catNames = {all:'Toutes les annonces',phones:'📱 Téléphones',mode:'👗 Mode',motos:'🛵 Motos',voitures:'🚗 Voitures',immo:'🏠 Immobilier',meubles:'🛋️ Meubles',info:'🖥️ Informatique',sport:'⚽ Sport',alim:'🍎 Alimentation',autres:'💼 Autres'};
  if(breadcrumb) breadcrumb.textContent = q ? `Résultats pour "${q}"` : catNames[currentCat]||'Annonces';
  if(count) count.innerHTML = `<b>${ads.length}</b> résultat${ads.length>1?'s':''}`;

  if (ads.length===0) {
    grid.innerHTML=`<div class="empty-state" style="grid-column:1/-1"><div class="empty-ico">🔍</div><div class="empty-title">Aucun résultat</div><div class="empty-sub">Essayez une autre recherche ou publiez votre annonce !</div></div>`;
  } else {
    grid.innerHTML = ads.map(a=>renderCard(a)).join('');
  }
}

/* ═══════════════ PRODUCT DETAIL ═══════════════ */
function openProduct(id) {
  const ad = state.ads.find(a=>a.id===id);
  if (!ad) return;
  document.getElementById('det-breadcrumb').textContent = ad.title;
  document.getElementById('det-price').textContent = Number(ad.price).toLocaleString('fr-FR') + ' FCFA';
  document.getElementById('det-name').textContent = ad.title;
  document.getElementById('det-desc').textContent = ad.desc || 'Aucune description.';
  document.getElementById('det-meta').innerHTML = `<span>🗂️ ${ad.cat}</span><span>📍 ${ad.lieu||'Bouaké'}</span><span>📅 Récent</span>`;
  const mainImg = document.getElementById('det-main-img');
  mainImg.innerHTML = ad.img ? `<img src="${ad.img}" alt="${ad.title}"/>` : `<span style="font-size:6rem">${ad.emoji||'📦'}</span>`;
  document.getElementById('det-thumbs').innerHTML = `<div class="prod-thumb active">${ad.img?`<img src="${ad.img}"/>`:(ad.emoji||'📦')}</div>`;
  // seller
  const sel = ad.seller || {};
  const selAv = document.getElementById('det-seller-av');
  if (sel.avatarUrl) selAv.innerHTML=`<img src="${sel.avatarUrl}" alt="av"/>`;
  else selAv.textContent = (sel.name||'V').charAt(0).toUpperCase();
  document.getElementById('det-seller-name').textContent = sel.name||'Vendeur';
  document.getElementById('det-seller-loc').textContent = '📍 '+( ad.lieu||'Bouaké');
  // WA button
  const waBtn = document.getElementById('det-wa-btn');
  const waNum = '225'+( sel.phone||'0700000000').replace(/\s/g,'');
  const waMsg = encodeURIComponent(`Bonjour ! Je suis intéressé(e) par votre annonce "${ad.title}" à ${Number(ad.price).toLocaleString('fr-FR')} FCFA sur JFK Service Bouaké.`);
  waBtn.onclick = () => window.open(`https://wa.me/${waNum}?text=${waMsg}`,'_blank');
  showPage('product');
}

function toggleFav() { toast('❤️ Annonce sauvegardée dans vos favoris !','or'); }

function toggleFavItem(id, e) {
  e.stopPropagation();
  const idx = state.favs.indexOf(id);
  if (idx>=0) state.favs.splice(idx,1);
  else state.favs.push(id);
  saveState();
  const count = document.getElementById('fav-count');
  if(count) count.textContent = state.favs.length;
  e.target.textContent = state.favs.includes(id) ? '❤️' : '🤍';
  toast(state.favs.includes(id)?'❤️ Ajouté aux favoris !':'🤍 Retiré des favoris');
}

function waContact(id, e) {
  e.stopPropagation();
  const ad = state.ads.find(a=>a.id===id);
  if (!ad) return;
  const waNum = '225'+(ad.seller?.phone||'0700000000').replace(/\s/g,'');
  const msg = encodeURIComponent(`Bonjour ! Je suis intéressé(e) par votre annonce "${ad.title}" à ${Number(ad.price).toLocaleString('fr-FR')} FCFA sur JFK Service Bouaké.`);
  window.open(`https://wa.me/${waNum}?text=${msg}`,'_blank');
  toast('💬 Ouverture WhatsApp...','wa');
}

/* ═══════════════ DASHBOARD ═══════════════ */
function renderDashboard() {
  const u = state.currentUser;
  if (!u) return;
  // Sidebar
  const avEl = document.getElementById('dash-av-lg');
  if(u.avatarUrl) avEl.innerHTML=`<img src="${u.avatarUrl}" alt="av" style="width:100%;height:100%;object-fit:cover;border-radius:50%"/>`;
  else { avEl.textContent=u.name.charAt(0).toUpperCase(); avEl.style.background='var(--gr)'; }
  document.getElementById('dash-name-lg').textContent = u.name;
  document.getElementById('dash-email-sm').textContent = u.email;
  document.getElementById('dash-hello').textContent = u.name.split(' ')[0];
  // Stats
  const myAds = state.ads.filter(a=>a.sellerId===u.id);
  document.getElementById('my-ads-count').textContent = myAds.length;
  document.getElementById('my-views').textContent = myAds.length * 7;
  document.getElementById('my-contacts').textContent = myAds.length * 2;
  document.getElementById('my-favs-count').textContent = state.favs.length;
  // Profile block
  document.getElementById('profile-info-block').innerHTML = `
    📛 <b>Nom :</b> ${u.name}<br>
    ✉️ <b>Email :</b> ${u.email}<br>
    📲 <b>WhatsApp :</b> +225 ${u.phone||'—'}<br>
    📍 <b>Quartier :</b> ${u.quartier||'—'}<br>
    🗓️ <b>Inscrit le :</b> ${new Date(u.createdAt).toLocaleDateString('fr-FR')}`;
  // Profile tab
  const paBig = document.getElementById('profile-av-big');
  if(u.avatarUrl) paBig.innerHTML=`<img src="${u.avatarUrl}" alt="av" style="width:100%;height:100%;object-fit:cover;border-radius:50%"/>`;
  else { paBig.textContent=u.name.charAt(0).toUpperCase(); }
  document.getElementById('profile-name-big').textContent = u.name;
  document.getElementById('profile-phone-big').textContent = '📲 +225 '+(u.phone||'—');
  document.getElementById('profile-email-big').textContent = '✉️ '+u.email;
  document.getElementById('profile-details').innerHTML = `📍 <b>Quartier :</b> ${u.quartier||'—'}<br>🗓️ <b>Inscrit le :</b> ${new Date(u.createdAt).toLocaleDateString('fr-FR')}<br>✅ <b>WhatsApp vérifié</b>`;
  // My ads
  renderMyAds();
  // Favs
  renderFavs();
  // Prefill publish form
  const pfWa = document.getElementById('pf-wa');
  const pfSel = document.getElementById('pf-seller-name');
  if (pfWa && !pfWa.value) pfWa.value = u.phone||'';
  if (pfSel && !pfSel.value) pfSel.value = u.name||'';
  // Build photo upload slots
  buildPfSlots();
}

function showDashTab(tab, btn) {
  ['overview','myads','publish','profile','favs'].forEach(t => {
    const el = document.getElementById('tab-'+t);
    if(el) el.style.display = t===tab?'block':'none';
  });
  document.querySelectorAll('.dash-menu-item').forEach(i=>i.classList.remove('active-menu'));
  if (btn) btn.classList.add('active-menu');
  if (tab==='publish') buildPfSlots();
  if (tab==='myads') renderMyAds();
  if (tab==='favs') renderFavs();
}

function renderMyAds() {
  const u = state.currentUser; if(!u) return;
  const myAds = state.ads.filter(a=>a.sellerId===u.id);
  const grid = document.getElementById('my-ads-grid');
  if (myAds.length===0) {
    grid.innerHTML=`<div class="empty-state" style="grid-column:1/-1"><div class="empty-ico">📭</div><div class="empty-title">Aucune annonce</div><div class="empty-sub">Publiez votre première annonce !</div></div>`;
    return;
  }
  grid.innerHTML = myAds.map(ad => `
    <div class="my-ad-card">
      <div class="my-ad-img">${ad.img?`<img src="${ad.img}" alt="${ad.title}"/>`:(ad.emoji||'📦')}</div>
      <div class="my-ad-body">
        <div class="my-ad-title">${ad.title}</div>
        <div class="my-ad-price">${Number(ad.price).toLocaleString('fr-FR')} FCFA</div>
        <div class="my-ad-meta">📍 ${ad.lieu||'Bouaké'}</div>
        <div class="my-ad-actions">
          <button class="ad-act-btn" onclick="openProduct('${ad.id}')">👁 Voir</button>
          <button class="ad-act-btn ad-act-del" onclick="deleteAd('${ad.id}')">🗑 Suppr.</button>
        </div>
      </div>
    </div>`).join('');
}

function deleteAd(id) {
  if (!confirm('Supprimer cette annonce ?')) return;
  state.ads = state.ads.filter(a=>a.id!==id);
  saveState();
  renderMyAds();
  renderHomepage();
  toast('🗑️ Annonce supprimée','err');
}

function renderFavs() {
  const grid = document.getElementById('favs-grid');
  const favAds = state.ads.filter(a=>state.favs.includes(a.id));
  if (favAds.length===0) {
    grid.innerHTML=`<div class="empty-state" style="grid-column:1/-1"><div class="empty-ico">💔</div><div class="empty-title">Aucun favori</div><div class="empty-sub">Cliquez sur ❤️ sur une annonce</div></div>`;
    return;
  }
  grid.innerHTML = favAds.map(a=>renderCard(a,true)).join('');
}

/* ═══════════════ PUBLISH FORM ═══════════════ */
let pfPhotos = []; const MAX_PH = 6;

function buildPfSlots() {
  const grid = document.getElementById('pub-photo-grid');
  if (!grid) return;
  grid.innerHTML='';
  pfPhotos = new Array(MAX_PH).fill(null);
  for (let i=0;i<MAX_PH;i++) {
    const s = document.createElement('div');
    s.className='photo-slot-up'; s.id='pfs'+i;
    s.innerHTML=`<div style="font-size:1.4rem;opacity:.35">📷</div><div style="font-size:.62rem;color:var(--muted);margin-top:4px">Photo ${i+1}</div><input type="file" accept="image/*" style="display:none" id="pfi${i}" onchange="pfSetPhoto(${i},this)"/><button class="psrm" onclick="pfRm(${i},event)">✕</button>`;
    s.addEventListener('click',e=>{if(!e.target.classList.contains('psrm'))document.getElementById('pfi'+i).click();});
    grid.appendChild(s);
  }
}

function pfSetPhoto(i,inp) {
  if(!inp.files[0]) return;
  const r=new FileReader();r.onload=e=>{
    pfPhotos[i]=e.target.result;
    const s=document.getElementById('pfs'+i);s.classList.add('has');
    s.querySelector('div').style.display='none';s.querySelectorAll('div')[1].style.display='none';
    let img=s.querySelector('img');if(!img){img=document.createElement('img');s.insertBefore(img,s.querySelector('.psrm'));}
    img.src=e.target.result;toast('✅ Photo ajoutée !');
  };r.readAsDataURL(inp.files[0]);
}
function pfRm(i,e) {
  e.stopPropagation();pfPhotos[i]=null;
  const s=document.getElementById('pfs'+i);s.classList.remove('has');
  const img=s.querySelector('img');if(img)img.remove();
  s.querySelectorAll('div').forEach(d=>d.style.display='');
}

function pfSetStep(n) {
  [1,2,3,4].forEach(i=>{
    const step=document.getElementById('pstep'+i);const sec=document.getElementById('pf'+i);
    if(!step||!sec) return;
    step.classList.remove('ps-active','done');
    if(i<n) step.classList.add('done');
    if(i===n) step.classList.add('ps-active');
    step.querySelector('.ps-circle').textContent=i<n?'✓':i;
    sec.classList.remove('pf-active');
  });
  const active=document.getElementById('pf'+n);if(active)active.classList.add('pf-active');
}

function pfNext(n) {
  if(n===2) {/* photos can be empty, OK */}
  if(n===3) {
    const title=document.getElementById('pf-title').value.trim();
    const price=document.getElementById('pf-price').value;
    const cat=document.getElementById('pf-cat').value;
    if(!cat){toast('⚠️ Choisissez une catégorie','err');return;}
    if(!title){toast('⚠️ Entrez un titre','err');return;}
    if(!price||Number(price)<=0){toast('⚠️ Entrez un prix valide','err');return;}
  }
  if(n===4) buildPfPreview();
  pfSetStep(n);
}
function pfBack(n){pfSetStep(n);}

function buildPfPreview() {
  const price=document.getElementById('pf-price').value;
  const title=document.getElementById('pf-title').value||'—';
  const desc=document.getElementById('pf-desc').value||'Aucune description.';
  const cat=document.getElementById('pf-cat').value||'—';
  const lieu=document.getElementById('pf-lieu').value||'Bouaké';
  const wa=document.getElementById('pf-wa').value||'—';
  const seller=document.getElementById('pf-seller-name').value||(state.currentUser?.name||'Vendeur');
  document.getElementById('pf-prev-price').textContent=price?Number(price).toLocaleString('fr-FR')+' FCFA':'—';
  document.getElementById('pf-prev-title').textContent=title;
  document.getElementById('pf-prev-meta').textContent=cat+' • 📍 '+lieu+' • '+seller;
  document.getElementById('pf-prev-desc').textContent=desc;
  document.getElementById('pf-prev-wa').textContent='+225 '+wa;
  const pi=document.getElementById('pf-prev-img');
  const firstPhoto=pfPhotos.find(p=>p!==null);
  pi.innerHTML=firstPhoto?`<img src="${firstPhoto}" alt="prev" style="width:100%;height:100%;object-fit:cover;position:absolute;inset:0"/>`:'<span style="font-size:4rem">📦</span>';
}

function publishAd() {
  const u=state.currentUser;
  if(!u){openOverlay('login');return;}
  const title=document.getElementById('pf-title').value.trim();
  const price=document.getElementById('pf-price').value;
  const cat=document.getElementById('pf-cat').value;
  const desc=document.getElementById('pf-desc').value.trim();
  const lieu=document.getElementById('pf-lieu').value.trim();
  const wa=document.getElementById('pf-wa').value.trim();
  const sellerName=document.getElementById('pf-seller-name').value.trim()||u.name;
  const firstPhoto=pfPhotos.find(p=>p!==null)||null;
  const catEmojis={phones:'📱',info:'💻',mode:'👗',motos:'🛵',voitures:'🚗',immo:'🏠',meubles:'🛋️',sport:'⚽',alim:'🍎',autres:'💼'};
  const ad = {
    id:'a'+Date.now(),
    title, price:Number(price), cat, desc, lieu,
    img:firstPhoto, emoji:catEmojis[cat]||'📦',
    badge:'NEW', createdAt:Date.now(),
    sellerId:u.id,
    seller:{name:sellerName,phone:wa||u.phone,avatarUrl:u.avatarUrl}
  };
  state.ads.unshift(ad);
  saveState();
  toast('🚀 Annonce publiée ! Elle est maintenant visible sur la page d\'accueil.','wa',4000);
  // Reset form
  pfSetStep(1);
  buildPfSlots();
  ['pf-title','pf-price','pf-desc','pf-lieu'].forEach(id=>{const el=document.getElementById(id);if(el)el.value='';});
  document.getElementById('pf-cat').value='';
  showDashTab('myads',null);
  renderHomepage();
  renderMyAds();
  updateStatsBand();
}

/* ═══════════════ DATE ═══════════════ */
document.getElementById('tb-date').textContent = new Date().toLocaleDateString('fr-FR',{weekday:'short',day:'numeric',month:'long'});

/* ═══════════════ INIT ═══════════════ */
updateNav();
renderHomepage();
  </script>
</body>

</html>
