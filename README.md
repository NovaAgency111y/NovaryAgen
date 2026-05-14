
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Novary Agency - Jasa Pembuatan Website Profesional</title>
    <meta name="description" content="Novary Agency - Jasa pembuatan website profesional, modern, dan responsif. Mulai dari 100K saja!">
    <link href="https://cdn.jsdelivr.net/npm/remixicon@4.2.0/fonts/remixicon.css" rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        /* ===== CSS VARIABLES ===== */
        :root {
            --bg-primary: #0a0a0f;
            --bg-secondary: #12121a;
            --bg-card: #1a1a24;
            --text-primary: #ffffff;
            --text-secondary: #a0a0b0;
            --neon-blue: #00d4ff;
            --neon-blue-glow: rgba(0, 212, 255, 0.3);
            --neon-orange: #ff6b35;
            --neon-orange-glow: rgba(255, 107, 53, 0.3);
            --gradient-blue: linear-gradient(135deg, #00d4ff 0%, #0099cc 100%);
            --gradient-orange: linear-gradient(135deg, #ff6b35 0%, #ff8c5a 100%);
            --border-color: rgba(255, 255, 255, 0.08);
            --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            min-height: 100vh;
        }

        a { text-decoration: none; color: inherit; }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            font-size: clamp(1.6rem, 4vw, 2.5rem);
            font-weight: 700;
            margin-bottom: 16px;
            letter-spacing: -0.02em;
        }

        .section-subtitle {
            color: var(--text-secondary);
            font-size: 1rem;
            max-width: 600px;
            line-height: 1.7;
        }

        .highlight { color: var(--neon-blue); }
        .highlight-orange { color: var(--neon-orange); }
        .text-center { text-align: center; }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            padding: 12px 24px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            text-decoration: none;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            white-space: nowrap;
        }

        .btn-primary {
            background: var(--gradient-blue);
            color: var(--bg-primary);
            box-shadow: 0 4px 20px var(--neon-blue-glow);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px var(--neon-blue-glow);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-primary);
            border: 1px solid var(--border-color);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.05);
            border-color: var(--neon-blue);
        }

        .btn-orange {
            background: var(--gradient-orange);
            color: white;
            box-shadow: 0 4px 20px var(--neon-orange-glow);
        }

        .btn-orange:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px var(--neon-orange-glow);
        }

        /* ===== DEVICE MODE SWITCHER ===== */
        .device-switcher {
            position: fixed;
            top: 80px;
            right: 20px;
            z-index: 1001;
            display: flex;
            flex-direction: column;
            gap: 8px;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 12px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            opacity: 0;
            visibility: hidden;
            transform: translateY(-10px);
            transition: var(--transition);
        }

        .device-switcher.active {
            opacity: 1;
            visibility: visible;
            transform: translateY(0);
        }

        .device-switcher-btn {
            position: fixed;
            top: 80px;
            right: 20px;
            z-index: 1002;
            width: 50px;
            height: 50px;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 14px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--neon-blue);
            font-size: 1.3rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .device-switcher-btn:hover {
            background: var(--gradient-blue);
            color: var(--bg-primary);
            border-color: transparent;
        }

        .device-switcher-btn.active {
            background: var(--gradient-blue);
            color: var(--bg-primary);
            border-color: transparent;
        }

        .device-option {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px 14px;
            border-radius: 10px;
            cursor: pointer;
            transition: var(--transition);
            font-size: 0.85rem;
            font-weight: 500;
            color: var(--text-secondary);
        }

        .device-option:hover {
            background: rgba(0, 212, 255, 0.1);
            color: var(--text-primary);
        }

        .device-option.active {
            background: rgba(0, 212, 255, 0.15);
            color: var(--neon-blue);
        }

        .device-option i {
            font-size: 1.2rem;
        }

        /* ===== NAVIGATION ===== */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 16px 0;
            transition: var(--transition);
        }

        nav.scrolled {
            background: rgba(10, 10, 15, 0.95);
            backdrop-filter: blur(20px);
            padding: 10px 0;
            border-bottom: 1px solid var(--border-color);
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.2rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .logo-icon {
            width: 34px;
            height: 34px;
            background: var(--gradient-blue);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
            color: var(--bg-primary);
        }

        .logo span {
            background: var(--gradient-blue);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 24px;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            font-weight: 500;
            font-size: 0.9rem;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--neon-blue);
            transition: var(--transition);
        }

        .nav-links a:hover { color: var(--text-primary); }
        .nav-links a:hover::after { width: 100%; }

        .nav-cta { padding: 8px 16px; font-size: 0.85rem; }

        .mobile-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            padding: 8px;
            background: none;
            border: none;
            z-index: 1003;
        }

        .mobile-toggle span {
            width: 22px;
            height: 2px;
            background: var(--text-primary);
            transition: var(--transition);
            display: block;
        }

        .mobile-toggle.active span:nth-child(1) {
            transform: rotate(45deg) translate(5px, 5px);
        }

        .mobile-toggle.active span:nth-child(2) { opacity: 0; }

        .mobile-toggle.active span:nth-child(3) {
            transform: rotate(-45deg) translate(5px, -5px);
        }

        .mobile-menu {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(10, 10, 15, 0.98);
            backdrop-filter: blur(20px);
            z-index: 999;
            padding: 80px 20px 30px;
            flex-direction: column;
            gap: 6px;
            overflow-y: auto;
        }

        .mobile-menu.active { display: flex; }

        .mobile-menu a {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--text-primary);
            padding: 14px 0;
            border-bottom: 1px solid var(--border-color);
            transition: var(--transition);
        }

        .mobile-menu a:hover { color: var(--neon-blue); }
        .mobile-menu .btn { margin-top: 20px; }

        /* ===== HERO SECTION ===== */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            padding: 100px 0 60px;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -20%;
            right: -10%;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, var(--neon-blue-glow) 0%, transparent 70%);
            filter: blur(80px);
            animation: pulse 8s ease-in-out infinite;
            pointer-events: none;
        }

        .hero::after {
            content: '';
            position: absolute;
            bottom: -10%;
            left: -10%;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, var(--neon-orange-glow) 0%, transparent 70%);
            filter: blur(100px);
            animation: pulse 10s ease-in-out infinite reverse;
            pointer-events: none;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.4; transform: scale(1); }
            50% { opacity: 0.7; transform: scale(1.1); }
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-content { animation: fadeInUp 0.8s ease; }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 6px 12px;
            background: rgba(0, 212, 255, 0.1);
            border: 1px solid rgba(0, 212, 255, 0.2);
            border-radius: 50px;
            font-size: 0.8rem;
            color: var(--neon-blue);
            margin-bottom: 20px;
        }

        .hero h1 {
            font-size: clamp(1.8rem, 4vw, 2.8rem);
            font-weight: 800;
            line-height: 1.2;
            margin-bottom: 16px;
            letter-spacing: -0.02em;
        }

        .hero h1 .gradient-text {
            background: var(--gradient-blue);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1rem;
            color: var(--text-secondary);
            margin-bottom: 24px;
            max-width: 480px;
            line-height: 1.7;
        }

        .hero-buttons {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .hero-stats {
            display: flex;
            gap: 30px;
            margin-top: 36px;
            padding-top: 24px;
            border-top: 1px solid var(--border-color);
        }

        .stat-number {
            font-size: 1.6rem;
            font-weight: 700;
            color: var(--neon-blue);
        }

        .stat-label {
            font-size: 0.8rem;
            color: var(--text-secondary);
            margin-top: 2px;
        }

        .hero-visual { position: relative; animation: fadeInUp 0.8s ease 0.2s both; }

        .hero-image-wrapper {
            position: relative;
            width: 100%;
            max-width: 420px;
            margin: 0 auto;
        }

        .hero-browser {
            background: var(--bg-card);
            border-radius: 14px;
            overflow: hidden;
            border: 1px solid var(--border-color);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
        }

        .browser-header {
            display: flex;
            align-items: center;
            gap: 6px;
            padding: 10px 14px;
            background: var(--bg-secondary);
            border-bottom: 1px solid var(--border-color);
        }

        .browser-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
        }

        .browser-dot.red { background: #ff5f57; }
        .browser-dot.yellow { background: #febc2e; }
        .browser-dot.green { background: #28c840; }

        .browser-content {
            padding: 20px;
            min-height: 220px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .browser-placeholder {
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .placeholder-box {
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1) 0%, rgba(0, 212, 255, 0.05) 100%);
            border: 1px solid rgba(0, 212, 255, 0.2);
            border-radius: 6px;
        }

        .placeholder-box.hero-main { height: 50px; }

        .placeholder-row { display: flex; gap: 12px; }

        .placeholder-box.small {
            flex: 1;
            height: 38px;
        }

        .floating-elements {
            position: absolute;
            top: -10px;
            right: -20px;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-12px) rotate(3deg); }
        }

        .floating-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 10px 14px;
            backdrop-filter: blur(10px);
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 10px;
        }

        .floating-card i { font-size: 1rem; color: var(--neon-blue); }

        .floating-card span {
            font-size: 0.75rem;
            font-weight: 600;
            white-space: nowrap;
        }

                /* ===== SERVICES SECTION ===== */
        .services {
            padding: 80px 0;
            position: relative;
        }

        .services::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, var(--neon-blue-glow) 0%, transparent 70%);
            filter: blur(100px);
            opacity: 0.2;
            pointer-events: none;
        }

        .services-header {
            text-align: center;
            margin-bottom: 48px;
            position: relative;
            z-index: 1;
        }

        .services-header .section-subtitle { margin: 0 auto; }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            position: relative;
            z-index: 1;
        }

        .service-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 24px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: var(--gradient-blue);
            transform: scaleX(0);
            transform-origin: left;
            transition: var(--transition);
        }

        .service-card:hover {
            transform: translateY(-6px);
            border-color: rgba(0, 212, 255, 0.3);
            box-shadow: 0 16px 32px rgba(0, 0, 0, 0.3);
        }

        .service-card:hover::before { transform: scaleX(1); }

        .service-icon {
            width: 48px;
            height: 48px;
            background: rgba(0, 212, 255, 0.1);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 16px;
            font-size: 1.2rem;
            color: var(--neon-blue);
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            background: var(--gradient-blue);
            color: var(--bg-primary);
        }

        .service-card h3 {
            font-size: 1.05rem;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .service-card p {
            color: var(--text-secondary);
            font-size: 0.85rem;
            line-height: 1.6;
        }

        /* ===== BONUS SECTION ===== */
        .bonus {
            padding: 80px 0;
        }

        .bonus-card {
            background: linear-gradient(135deg, var(--bg-card) 0%, var(--bg-secondary) 100%);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 48px 32px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .bonus-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at top right, var(--neon-orange-glow) 0%, transparent 50%);
            opacity: 0.3;
            pointer-events: none;
        }

        .bonus-content {
            position: relative;
            z-index: 1;
        }

        .bonus-icon {
            font-size: 3rem;
            color: var(--neon-orange);
            margin-bottom: 20px;
            display: inline-block;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-8px); }
        }

        .bonus-badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 6px 12px;
            background: rgba(255, 107, 53, 0.1);
            border: 1px solid rgba(255, 107, 53, 0.3);
            border-radius: 50px;
            font-size: 0.8rem;
            color: var(--neon-orange);
            margin-bottom: 16px;
        }

        .bonus-title {
            font-size: clamp(1.5rem, 4vw, 2.4rem);
            font-weight: 800;
            margin-bottom: 12px;
            line-height: 1.3;
        }

        .bonus-title .highlight-orange {
            background: var(--gradient-orange);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .bonus-description {
            color: var(--text-secondary);
            font-size: 0.95rem;
            max-width: 450px;
            margin: 0 auto 24px;
            line-height: 1.7;
        }

        /* ===== ADVANTAGES SECTION ===== */
        .advantages {
            padding: 80px 0;
            background: var(--bg-secondary);
        }

        .advantages-header {
            text-align: center;
            margin-bottom: 48px;
        }

        .advantages-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 16px;
        }

        .advantage-card {
            text-align: center;
            padding: 24px 16px;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 14px;
            transition: var(--transition);
        }

        .advantage-card:hover {
            transform: translateY(-4px);
            border-color: var(--neon-blue);
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.3);
        }

        .advantage-icon {
            width: 56px;
            height: 56px;
            background: rgba(0, 212, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 16px;
            font-size: 1.4rem;
            color: var(--neon-blue);
            transition: var(--transition);
        }

        .advantage-card:hover .advantage-icon {
            background: var(--gradient-blue);
            color: var(--bg-primary);
        }

        .advantage-card h3 {
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 6px;
        }

        .advantage-card p {
            font-size: 0.8rem;
            color: var(--text-secondary);
            line-height: 1.5;
        }

        /* ===== QUOTE SECTION ===== */
        .quote {
            padding: 80px 0;
            text-align: center;
            position: relative;
        }

        .quote::before {
            content: '"';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 12rem;
            font-family: Georgia, serif;
            color: rgba(0, 212, 255, 0.04);
            line-height: 1;
            pointer-events: none;
        }

        .quote-content {
            position: relative;
            z-index: 1;
            max-width: 700px;
            margin: 0 auto;
        }

        .quote blockquote {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            font-weight: 600;
            font-style: italic;
            margin-bottom: 20px;
            line-height: 1.4;
        }

        .quote-author {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .quote-author::before {
            content: '';
            width: 30px;
            height: 2px;
            background: var(--neon-blue);
        }

        /* ===== TESTIMONIALS SECTION ===== */
        .testimonials {
            padding: 80px 0;
            background: var(--bg-secondary);
        }

        .testimonials-header {
            text-align: center;
            margin-bottom: 48px;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
        }

        .testimonial-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 24px;
            transition: var(--transition);
            position: relative;
        }

        .testimonial-card:hover {
            transform: translateY(-4px);
            border-color: rgba(0, 212, 255, 0.3);
        }

        .testimonial-badge {
            position: absolute;
            top: 16px;
            right: 16px;
            padding: 4px 10px;
            background: rgba(0, 212, 255, 0.1);
            border-radius: 20px;
            font-size: 0.7rem;
            color: var(--neon-blue);
        }

        .testimonial-rating {
            display: flex;
            gap: 3px;
            margin-bottom: 12px;
        }

        .testimonial-rating i {
            color: #ffc107;
            font-size: 1rem;
        }

        .testimonial-text {
            font-size: 0.9rem;
            line-height: 1.7;
            color: var(--text-secondary);
            margin-bottom: 20px;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .testimonial-avatar {
            width: 44px;
            height: 44px;
            border-radius: 50%;
            background: var(--gradient-blue);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1rem;
            color: var(--bg-primary);
        }

        .testimonial-info h4 {
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 2px;
        }

        .testimonial-info p {
            font-size: 0.8rem;
            color: var(--text-secondary);
        }

        /* ===== CTA SECTION ===== */
        .cta {
            padding: 80px 0;
        }

        .cta-card {
            background: linear-gradient(135deg, var(--bg-card) 0%, var(--bg-secondary) 100%);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 60px 32px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at center, var(--neon-blue-glow) 0%, transparent 60%);
            opacity: 0.2;
            pointer-events: none;
        }

        .cta-content {
            position: relative;
            z-index: 1;
        }

        .cta h2 {
            font-size: clamp(1.6rem, 4vw, 2.4rem);
            font-weight: 700;
            margin-bottom: 12px;
        }

        .cta p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            max-width: 450px;
            margin: 0 auto 24px;
            line-height: 1.7;
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 12px;
            flex-wrap: wrap;
        }

        /* ===== FOOTER ===== */
        footer {
            background: var(--bg-secondary);
            padding: 48px 0 24px;
            border-top: 1px solid var(--border-color);
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .footer-brand {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-brand .logo-icon {
            width: 32px;
            height: 32px;
            font-size: 0.9rem;
        }

        .footer-brand h3 {
            font-size: 1.1rem;
            font-weight: 700;
        }

        .footer-social {
            display: flex;
            gap: 12px;
        }

        .footer-social a {
            width: 40px;
            height: 40px;
            border-radius: 10px;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-secondary);
            font-size: 1.1rem;
            transition: var(--transition);
        }

        .footer-social a:hover {
            background: var(--gradient-blue);
            border-color: transparent;
            color: var(--bg-primary);
        }

        .footer-bottom {
            margin-top: 32px;
            padding-top: 20px;
            border-top: 1px solid var(--border-color);
            text-align: center;
        }

        .footer-bottom p {
            color: var(--text-secondary);
            font-size: 0.85rem;
        }

        /* ===== SCROLL ANIMATIONS ===== */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* ===== FLOATING WHATSAPP BUTTON ===== */
        .floating-whatsapp {
            position: fixed;
            bottom: 24px;
            right: 24px;
            width: 56px;
            height: 56px;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.6rem;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            z-index: 998;
            transition: var(--transition);
            text-decoration: none;
        }

        .floating-whatsapp:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 30px rgba(37, 211, 102, 0.5);
        }

        .floating-whatsapp::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: #25D366;
            animation: whatsappPulse 2s ease-in-out infinite;
            z-index: -1;
        }

        @keyframes whatsappPulse {
            0% { transform: scale(1); opacity: 0.5; }
            100% { transform: scale(1.4); opacity: 0; }
        }

        /* ===== BACK TO TOP ===== */
        .back-to-top {
            position: fixed;
            bottom: 90px;
            right: 28px;
            width: 42px;
            height: 42px;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--neon-blue);
            font-size: 1.1rem;
            z-index: 997;
            transition: var(--transition);
            opacity: 0;
            visibility: hidden;
        }

        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            background: var(--gradient-blue);
            color: var(--bg-primary);
            border-color: transparent;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 1024px) {
            .hero-grid {
                grid-template-columns: 1fr;
                gap: 40px;
                text-align: center;
            }

            .hero-content { order: 1; }
            .hero-visual { order: 2; }

            .hero p { margin: 0 auto 24px; }
            .hero-buttons { justify-content: center; }
            .hero-stats { justify-content: center; }
            .hero-image-wrapper { max-width: 360px; }

            .services-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .advantages-grid {
                grid-template-columns: repeat(3, 1fr);
            }

            .testimonials-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .testimonials-grid .testimonial-card:last-child {
                grid-column: span 2;
                max-width: 50%;
                margin: 0 auto;
            }

            .cta-card { padding: 48px 32px; }

            .device-switcher {
                top: 70px;
                right: 16px;
            }

            .device-switcher-btn {
                top: 70px;
                right: 16px;
            }
        }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .nav-cta { display: none; }
            .mobile-toggle { display: flex; }

            .hero {
                padding: 90px 0 50px;
                min-height: auto;
            }

            .hero h1 { font-size: 1.8rem; }
            .hero p { font-size: 0.95rem; }
                        .hero-stats {
                flex-direction: column;
                gap: 16px;
            }

            .hero-image-wrapper { max-width: 300px; }
            .floating-elements { display: none; }

            .services-grid {
                grid-template-columns: 1fr;
            }

            .advantages-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 12px;
            }

            .advantage-card {
                padding: 20px 14px;
            }

            .advantage-icon {
                width: 50px;
                height: 50px;
                font-size: 1.2rem;
            }

            .bonus-card {
                padding: 36px 20px;
            }

            .bonus-icon { font-size: 2.5rem; }

            .testimonials-grid {
                grid-template-columns: 1fr;
            }

            .testimonials-grid .testimonial-card:last-child {
                grid-column: span 1;
                max-width: 100%;
            }

            .cta-card {
                padding: 40px 20px;
            }

            .footer-content {
                flex-direction: column;
                text-align: center;
            }

            .footer-brand {
                flex-direction: column;
            }

            .floating-whatsapp {
                bottom: 16px;
                right: 16px;
                width: 52px;
                height: 52px;
                font-size: 1.4rem;
            }

            .back-to-top {
                bottom: 78px;
                right: 20px;
                width: 38px;
                height: 38px;
                font-size: 1rem;
            }

            .device-switcher {
                top: 70px;
                right: 12px;
                padding: 10px;
            }

            .device-switcher-btn {
                top: 70px;
                right: 12px;
                width: 44px;
                height: 44px;
                font-size: 1.1rem;
            }
        }

        @media (max-width: 480px) {
            .container { padding: 0 16px; }

            .hero-buttons {
                flex-direction: column;
            }

            .hero-buttons .btn {
                width: 100%;
            }

            .advantages-grid {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .cta-buttons .btn {
                width: 100%;
            }

            .quote blockquote { font-size: 1.1rem; }

            .quote::before { font-size: 8rem; }

            .section-title { font-size: 1.5rem; }
        }
    </style>
</head>
<body>
    <!-- NAVIGATION -->
    <nav id="navbar">
        <div class="container nav-content">
            <a href="#" class="logo">
                <div class="logo-icon">
                    <i class="ri-global-line"></i>
                </div>
                <span>Novary Agency</span>
            </a>
            <ul class="nav-links">
                <li><a href="#services">Layanan</a></li>
                <li><a href="#advantages">Keunggulan</a></li>
                <li><a href="#testimonials">Testimoni</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
            <a href="https://wa.me/6285123231065" class="btn btn-primary nav-cta">
                <i class="ri-whatsapp-line"></i> Chat
            </a>
            <button class="mobile-toggle" id="mobileToggle" aria-label="Toggle menu">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
    </nav>

    <!-- MOBILE MENU -->
    <div class="mobile-menu" id="mobileMenu">
        <a href="#services" onclick="closeMobileMenu()">Layanan</a>
        <a href="#advantages" onclick="closeMobileMenu()">Keunggulan</a>
        <a href="#testimonials" onclick="closeMobileMenu()">Testimoni</a>
        <a href="#contact" onclick="closeMobileMenu()">Kontak</a>
        <a href="https://wa.me/6285123231065" class="btn btn-primary">
            <i class="ri-whatsapp-line"></i> Chat WhatsApp
        </a>
    </div>

    <!-- DEVICE SWITCHER -->
    <div class="device-switcher" id="deviceSwitcher">
        <div class="device-option" data-device="desktop" onclick="setDeviceMode('desktop')">
            <i class="ri-computer-line"></i>
            <span>Desktop</span>
        </div>
        <div class="device-option" data-device="tablet" onclick="setDeviceMode('tablet')">
            <i class="ri-tablet-line"></i>
            <span>Tablet</span>
        </div>
        <div class="device-option" data-device="mobile" onclick="setDeviceMode('mobile')">
            <i class="ri-smartphone-line"></i>
            <span>Mobile</span>
        </div>
    </div>
    <button class="device-switcher-btn" id="deviceSwitcherBtn" aria-label="Device Mode" onclick="toggleDeviceSwitcher()">
        <i class="ri-device-line"></i>
    </button>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-grid">
                <div class="hero-content">
                    <div class="hero-badge">
                        <i class="ri-sparkling-line"></i>
                        Jasa Website Profesional
                    </div>
                    <h1>
                        Website Modern Untuk<br>
                        <span class="gradient-text">Bisnis & Personal Branding</span>
                    </h1>
                    <p>Jasa pembuatan website profesional dengan desain modern, responsif, dan performa cepat. Mulai dari 100K saja!</p>
                    <div class="hero-buttons">
                        <a href="https://wa.me/6285123231065" class="btn btn-primary">
                            <i class="ri-whatsapp-line"></i> Chat WhatsApp
                        </a>
                        <a href="#services" class="btn btn-secondary">
                            <i class="ri-eye-line"></i> Lihat Layanan
                        </a>
                    </div>
                    <div class="hero-stats">
                        <div>
                            <div class="stat-number">150+</div>
                            <div class="stat-label">Project Selesai</div>
                        </div>
                        <div>
                            <div class="stat-number">100%</div>
                            <div class="stat-label">Client Puas</div>
                        </div>
                        <div>
                            <div class="stat-number">24/7</div>
                            <div class="stat-label">Support</div>
                        </div>
                    </div>
                </div>
                <div class="hero-visual">
                    <div class="hero-image-wrapper">
                        <div class="floating-elements">
                            <div class="floating-card">
                                <i class="ri-rocket-line"></i>
                                <span>Loading Fast</span>
                            </div>
                            <div class="floating-card">
                                <i class="ri-smartphone-line"></i>
                                <span>Mobile Friendly</span>
                            </div>
                        </div>
                        <div class="hero-browser">
                            <div class="browser-header">
                                <div class="browser-dot red"></div>
                                <div class="browser-dot yellow"></div>
                                <div class="browser-dot green"></div>
                            </div>
                            <div class="browser-content">
                                <div class="browser-placeholder">
                                    <div class="placeholder-box hero-main"></div>
                                    <div class="placeholder-row">
                                        <div class="placeholder-box small"></div>
                                        <div class="placeholder-box small"></div>
                                    </div>
                                    <div class="placeholder-row">
                                        <div class="placeholder-box small"></div>
                                        <div class="placeholder-box small"></div>
                                        <div class="placeholder-box small"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section class="services" id="services">
        <div class="container">
            <div class="services-header reveal">
                <h2 class="section-title">Layanan <span class="highlight">Kami</span></h2>
                <p class="section-subtitle">Berbagai layanan pembuatan website yang bisa disesuaikan dengan kebutuhan bisnis dan personal Anda.</p>
            </div>
            <div class="services-grid">
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="ri-pages-line"></i>
                    </div>
                    <h3>Landing Page</h3>
                    <p>Halaman landing page yang menarik dan fokus untuk konversi, cocok untuk campaign produk atau layanan Anda.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="ri-store-2-line"></i>
                    </div>
                    <h3>Website UMKM</h3>
                    <p>Website profesional untuk usaha kecil dan menengah dengan fitur lengkap untuk promosi dan penjualan.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="ri-user-star-line"></i>
                    </div>
                    <h3>Portfolio Website</h3>
                    <p>Tampilkan karya dan portofolio Anda dengan desain yang impressive untuk menarik klien potensial.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="ri-group-line"></i>
                    </div>
                    <h3>Website Komunitas</h3>
                    <p>Platform online untuk komunitas dengan fitur diskusi, agenda kegiatan, dan informasi terpusat.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="ri-smartphone-line"></i>
                    </div>
                    <h3>Responsive Design</h3>
                    <p>Desain yang menyesuaikan dengan semua ukuran layar, dari desktop hingga smartphone.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="ri-server-line"></i>
                    </div>
                    <h3>Setup Hosting</h3>
                    <p>Peniapan hosting dan domain agar website Anda bisa diakses di internet dengan cepat.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- BONUS SECTION -->
    <section class="bonus" id="bonus">
        <div class="container">
            <div class="bonus-card reveal">
                <div class="bonus-content">
                    <div class="bonus-icon">
                        <i class="ri-gift-line"></i>
                    </div>
                    <div class="bonus-badge">
                        <i class="ri-sparkling-line"></i>
                        PROMO SPESIAL
                    </div>
                    <h2 class="bonus-title">
                        FREE SETUP HOSTING untuk<br>
                        <span class="highlight-orange">pemesanan di atas 200K!</span>
                    </h2>
                    <p class="bonus-description">
                        Jangan sampai melewatkan promo ini! Dapatkan setup hosting gratis untuk setiap pemesanan website di atas 200 ribu rupiah.
                    </p>
                    <a href="https://wa.me/6285123231065" class="btn btn-orange">
                        <i class="ri-whatsapp-line"></i> Pesan Sekarang
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ADVANTAGES SECTION -->
    <section class="advantages" id="advantages">
        <div class="container">
            <div class="advantages-header reveal">
                <h2 class="section-title">Kenapa Memilih <span class="highlight">Kami?</span></h2>
                <p class="section-subtitle">Keunggulan yang membuat kami berbeda dari agency lainnya.</p>
            </div>
            <div class="advantages-grid">
                <div class="advantage-card reveal">
                    <div class="advantage-icon">
                        <i class="ri-time-line"></i>
                    </div>
                    <h3>Fast Response</h3>
                    <p>Respon cepat untuk setiap pertanyaan dan request Anda.</p>
                </div>
                <div class="advantage-card reveal">
                    <div class="advantage-icon">
                        <i class="ri-edit-line"></i>
                    </div>
                    <h3>Support & Revisi</h3>
                    <p>Revisi hingga puas dan support teknis setelah website jadi.</p>
                </div>
                <div class="advantage-card reveal">
                    <div class="advantage-icon">
                        <i class="ri-smartphone-line"></i>
                    </div>
                    <h3>Mobile Friendly</h3>
                    <p>Website optimal di semua perangkat, desktop hingga mobile.</p>
                </div>
                <div class="advantage-card reveal">
                    <div class="advantage-icon">
                        <i class="ri-palette-line"></i>
                    </div>
                    <h3>Desain Modern</h3>
                    <p>Tampilan profesional dengan desain yang selalu up-to-date.</p>
                </div>
                <div class="advantage-card reveal">
                    <div class="advantage-icon">
                        <i class="ri-speed-line"></i>
                    </div>
                    <h3>Loading Cepat</h3>
                    <p>Website dengan loading speed tinggi untuk pengalaman terbaik.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- QUOTE SECTION -->
    <section class="quote" id="quote">
        <div class="container">
            <div class="quote-content reveal">
                <blockquote>
                    "Website murah, bukan berarti isi dan pelayanannya murahan."
                </blockquote>
                <div class="quote-author">
                    <span>Novary Agency</span>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS SECTION -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="testimonials-header reveal">
                <h2 class="section-title">Apa Kata <span class="highlight">Mereka?</span></h2>
                <p class="section-subtitle">Testimoni dari klien yang sudah puas dengan layanan kami.</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card reveal">
                    <div class="testimonial-badge">Verified</div>
                    <div class="testimonial-rating">
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                    </div>
                    <p class="testimonial-text">
                        "Hasil website landing page-nya sangat memuaskan! Desainnya profesional dan loadingnya cepat. Recommended banget!"
                    </p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">RS</div>
                        <div class="testimonial-info">
                            <h4>Rizky Setiawan</h4>
                            <p>Owner Toko Online</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card reveal">
                    <div class="testimonial-badge">Verified</div>
                    <div class="testimonial-rating">
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                    </div>
                    <p class="testimonial-text">
                        "Portfolio website yang dibuat keren banget! Client baru langsung masuk setelah lihat portfolio online saya."
                    </p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">DA</div>
                        <div class="testimonial-info">
                            <h4>Dian Anggraini</h4>
                            <p>Freelance Designer</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card reveal">
                    <div class="testimonial-badge">Verified</div>
                    <div class="testimonial-rating">
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                        <i class="ri-star-fill"></i>
                    </div>
                    <p class="testimonial-text">
                        "Respons cepat dan revisi sampai puas! Website UMKM saya sekarang bisa diakses dengan domain sendiri."
                    </p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">BP</div>
                        <div class="testimonial-info">
                            <h4>Budi Prasetyo</h4>
                            <p>Pemilik Warung Makan</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA SECTION -->
    <section class="cta" id="contact">
        <div class="container">
            <div class="cta-card reveal">
                <div class="cta-content">
                    <h2>Siap Membuat Website Impian Anda?</h2>
                    <p>Jangan tunda lagi! Hubungi kami sekarang dan dapatkan website profesional dengan harga terjangkau.</p>
                    <div class="cta-buttons">
                        <a href="https://wa.me/6285123231065" class="btn btn-primary">
                            <i class="ri-whatsapp-line"></i> Chat WhatsApp
                        </a>
                        <a href="#services" class="btn btn-secondary">
                            <i class="ri-arrow-left-line"></i> Lihat Layanan
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-brand">
                                        <div class="logo-icon">
                        <i class="ri-global-line"></i>
                    </div>
                    <h3>Novary Agency</h3>
                </div>
                <div class="footer-social">
                    <a href="https://wa.me/6285123231065" aria-label="WhatsApp" target="_blank">
                        <i class="ri-whatsapp-line"></i>
                    </a>
                    <a href="#" aria-label="Instagram" target="_blank">
                        <i class="ri-instagram-line"></i>
                    </a>
                    <a href="#" aria-label="Email">
                        <i class="ri-mail-line"></i>
                    </a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Novary Agency. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- FLOATING WHATSAPP BUTTON -->
    <a href="https://wa.me/6285123231065" class="floating-whatsapp" aria-label="Chat WhatsApp" target="_blank">
        <i class="ri-whatsapp-line"></i>
    </a>

    <!-- BACK TO TOP BUTTON -->
    <a href="#" class="back-to-top" id="backToTop" aria-label="Back to top">
        <i class="ri-arrow-up-line"></i>
    </a>

    <!-- JAVASCRIPT -->
    <script>
        // Mobile Menu Toggle
        const mobileToggle = document.getElementById('mobileToggle');
        const mobileMenu = document.getElementById('mobileMenu');

        mobileToggle.addEventListener('click', function() {
            this.classList.toggle('active');
            mobileMenu.classList.toggle('active');
            document.body.style.overflow = mobileMenu.classList.contains('active') ? 'hidden' : '';
        });

        function closeMobileMenu() {
            mobileToggle.classList.remove('active');
            mobileMenu.classList.remove('active');
            document.body.style.overflow = '';
        }

        // Navbar Scroll Effect
        const navbar = document.getElementById('navbar');

        window.addEventListener('scroll', function() {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Back to Top Button
        const backToTop = document.getElementById('backToTop');

        window.addEventListener('scroll', function() {
            if (window.scrollY > 500) {
                backToTop.classList.add('visible');
            } else {
                backToTop.classList.remove('visible');
            }
        });

        backToTop.addEventListener('click', function(e) {
            e.preventDefault();
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        // Scroll Reveal Animation
        const revealElements = document.querySelectorAll('.reveal');

        function reveal() {
            revealElements.forEach(element => {
                const windowHeight = window.innerHeight;
                const elementTop = element.getBoundingClientRect().top;
                const revealPoint = 150;

                if (elementTop < windowHeight - revealPoint) {
                    element.classList.add('active');
                }
            });
        }

        window.addEventListener('scroll', reveal);
        window.addEventListener('load', reveal);

        // Smooth Scroll for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const href = this.getAttribute('href');
                if (href !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(href);
                    if (target) {
                        const offsetTop = target.offsetTop - 80;
                        window.scrollTo({
                            top: offsetTop,
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });

        // Device Mode Switcher
        const deviceSwitcher = document.getElementById('deviceSwitcher');
        const deviceSwitcherBtn = document.getElementById('deviceSwitcherBtn');
        let isDeviceSwitcherOpen = false;

        function toggleDeviceSwitcher() {
            isDeviceSwitcherOpen = !isDeviceSwitcherOpen;
            deviceSwitcher.classList.toggle('active', isDeviceSwitcherOpen);
            deviceSwitcherBtn.classList.toggle('active', isDeviceSwitcherOpen);
        }

        function setDeviceMode(device) {
            const deviceOptions = document.querySelectorAll('.device-option');
            deviceOptions.forEach(option => {
                option.classList.remove('active');
                if (option.dataset.device === device) {
                    option.classList.add('active');
                }
            });

            let maxWidth = '100%';
            let width = window.innerWidth;

            switch(device) {
                case 'desktop':
                    maxWidth = '100%';
                    break;
                case 'tablet':
                    maxWidth = '768px';
                    break;
                case 'mobile':
                    maxWidth = '480px';
                    break;
            }

            document.body.style.maxWidth = maxWidth;
            document.body.style.margin = '0 auto';
            document.body.style.background = 'var(--bg-primary)';

            // Close switcher after selection
            isDeviceSwitcherOpen = false;
            deviceSwitcher.classList.remove('active');
            deviceSwitcherBtn.classList.remove('active');
        }

        // Close device switcher when clicking outside
        document.addEventListener('click', function(e) {
            if (isDeviceSwitcherOpen && 
                !deviceSwitcher.contains(e.target) && 
                !deviceSwitcherBtn.contains(e.target)) {
                isDeviceSwitcherOpen = false;
                deviceSwitcher.classList.remove('active');
                deviceSwitcherBtn.classList.remove('active');
            }
        });

        // Initialize first device option as active
        document.querySelector('.device-option[data-device="desktop"]').classList.add('active');
    </script>
</body>
</html>
