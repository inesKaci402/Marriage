<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>💍 Julie & Antoine · Mariage</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet" />
    <style>
        /* ---------- RESET & BASE ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #fcf8f4;
            color: #2d2a24;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 24px;
            background-image:
                radial-gradient(circle at 15% 20%, rgba(235, 215, 195, 0.25) 0%, transparent 50%),
                radial-gradient(circle at 85% 80%, rgba(210, 180, 160, 0.2) 0%, transparent 50%),
                radial-gradient(circle at 50% 50%, rgba(245, 235, 225, 0.3) 0%, transparent 70%);
            animation: bgPulse 12s ease-in-out infinite alternate;
            position: relative;
            overflow-x: hidden;
        }

        /* Fond animé avec des formes flottantes */
        body::before,
        body::after {
            content: '';
            position: fixed;
            border-radius: 50%;
            opacity: 0.05;
            pointer-events: none;
            z-index: 0;
            animation: floatShape 20s infinite alternate ease-in-out;
        }
        body::before {
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, #e8d7cc, transparent 70%);
            top: -100px;
            left: -100px;
            animation-duration: 25s;
        }
        body::after {
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, #d9c8bc, transparent 70%);
            bottom: -150px;
            right: -150px;
            animation-duration: 30s;
            animation-delay: -5s;
        }

        @keyframes bgPulse {
            0% { background-size: 100% 100%; }
            100% { background-size: 120% 120%; }
        }

        @keyframes floatShape {
            0% { transform: translate(0, 0) scale(1) rotate(0deg); }
            100% { transform: translate(60px, 40px) scale(1.2) rotate(15deg); }
        }

        .card {
            max-width: 620px;
            width: 100%;
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(8px);
            border-radius: 48px 48px 36px 36px;
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.06), 0 15px 35px rgba(0, 0, 0, 0.04);
            overflow: hidden;
            position: relative;
            z-index: 1;
            animation: cardEntrance 0.9s cubic-bezier(0.23, 1, 0.32, 1) both;
            border: 1px solid rgba(255, 255, 255, 0.5);
            transition: transform 0.4s ease, box-shadow 0.4s ease;
        }

        .card:hover {
            transform: translateY(-6px) scale(1.005);
            box-shadow: 0 50px 100px rgba(0, 0, 0, 0.08), 0 20px 40px rgba(0, 0, 0, 0.05);
        }

        @keyframes cardEntrance {
            0% { opacity: 0; transform: translateY(40px) scale(0.96); }
            100% { opacity: 1; transform: translateY(0) scale(1); }
        }

        /* ---------- HERO / FLORAL TOP ---------- */
        .hero {
            background: linear-gradient(145deg, #f9f0e8, #f3e6db);
            padding: 40px 28px 32px;
            text-align: center;
            position: relative;
            border-bottom: 2px solid #e8d7cc;
            overflow: hidden;
        }

        .hero::after {
            content: "✦ ✦ ✦";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(255, 255, 255, 0.8);
            padding: 0 18px;
            font-size: 14px;
            letter-spacing: 8px;
            color: #b8a08e;
            backdrop-filter: blur(4px);
            border-radius: 20px;
        }

        /* fleurs animées en arrière-plan */
        .hero-bg-decoration {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 0;
        }

        .hero-bg-decoration span {
            position: absolute;
            font-size: 2.4rem;
            opacity: 0.12;
            animation: flowerFloat 18s infinite alternate ease-in-out;
        }
        .hero-bg-decoration span:nth-child(1) { top: 10%; left: 5%; animation-duration: 22s; }
        .hero-bg-decoration span:nth-child(2) { bottom: 15%; right: 8%; animation-duration: 26s; animation-delay: -4s; }
        .hero-bg-decoration span:nth-child(3) { top: 30%; right: 15%; animation-duration: 20s; animation-delay: -8s; }
        .hero-bg-decoration span:nth-child(4) { bottom: 30%; left: 12%; animation-duration: 24s; animation-delay: -2s; }

        @keyframes flowerFloat {
            0% { transform: translate(0, 0) rotate(0deg) scale(1); }
            33% { transform: translate(10px, -15px) rotate(6deg) scale(1.1); }
            66% { transform: translate(-8px, 10px) rotate(-4deg) scale(0.95); }
            100% { transform: translate(5px, -5px) rotate(2deg) scale(1.05); }
        }

        .floral-icon {
            font-size: 32px;
            letter-spacing: 8px;
            color: #b8a08e;
            margin-bottom: 6px;
            display: inline-block;
            animation: iconPulse 3s ease-in-out infinite;
        }

        @keyframes iconPulse {
            0%, 100% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.08); opacity: 1; }
        }

        .hero h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 3.6rem;
            font-weight: 400;
            color: #4a3a2e;
            line-height: 1.1;
            margin-bottom: 2px;
            position: relative;
            z-index: 1;
            text-shadow: 0 2px 10px rgba(255, 255, 255, 0.4);
            animation: fadeSlide 1s 0.2s both;
        }

        .hero .and {
            font-family: 'Inter', sans-serif;
            font-weight: 300;
            font-size: 1rem;
            letter-spacing: 6px;
            text-transform: uppercase;
            color: #b09886;
            margin: 2px 0 8px;
            position: relative;
            z-index: 1;
            animation: fadeSlide 1s 0.35s both;
        }

        .hero .date-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(6px);
            padding: 10px 28px;
            border-radius: 60px;
            font-size: 0.95rem;
            font-weight: 500;
            color: #4a3a2e;
            border: 1px solid rgba(255, 255, 255, 0.9);
            margin-top: 12px;
            letter-spacing: 0.5px;
            position: relative;
            z-index: 1;
            animation: fadeSlide 1s 0.5s both;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .hero .date-badge:hover {
            transform: scale(1.02);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.04);
        }

        .hero .date-badge span {
            font-weight: 300;
            color: #b09886;
        }

        @keyframes fadeSlide {
            0% { opacity: 0; transform: translateY(12px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        /* ---------- CONTENT ---------- */
        .content {
            padding: 40px 30px 34px;
        }

        .message {
            text-align: center;
            font-weight: 300;
            font-size: 1.05rem;
            line-height: 1.8;
            color: #4a3f38;
            margin-bottom: 30px;
            animation: fadeSlide 1s 0.6s both;
        }

        .message strong {
            font-weight: 600;
            color: #2d2a24;
        }

        /* ---------- COUNTDOWN ---------- */
        .countdown {
            display: flex;
            justify-content: center;
            gap: 14px;
            margin-bottom: 34px;
            flex-wrap: wrap;
            animation: fadeSlide 1s 0.7s both;
        }

        .countdown-item {
            background: rgba(249, 243, 238, 0.7);
            backdrop-filter: blur(4px);
            border-radius: 20px;
            padding: 14px 12px;
            min-width: 74px;
            text-align: center;
            border: 1px solid #efe4db;
            flex: 1 0 auto;
            transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.3s ease;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.02);
        }

        .countdown-item:hover {
            transform: translateY(-4px) scale(1.02);
            background: rgba(249, 243, 238, 0.95);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.06);
        }

        .countdown-item .number {
            font-family: 'Inter', sans-serif;
            font-size: 2.4rem;
            font-weight: 700;
            color: #4a3a2e;
            display: block;
            line-height: 1.2;
            letter-spacing: -0.5px;
            transition: transform 0.2s ease;
        }

        .countdown-item .number.flip {
            animation: popNumber 0.3s ease;
        }

        @keyframes popNumber {
            0% { transform: scale(1); }
            50% { transform: scale(1.15); color: #b09886; }
            100% { transform: scale(1); }
        }

        .countdown-item .label {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #b09886;
            font-weight: 400;
            margin-top: 4px;
        }

        /* ---------- DETAILS ---------- */
        .details {
            background: rgba(252, 248, 244, 0.7);
            backdrop-filter: blur(4px);
            border-radius: 24px;
            padding: 22px 24px;
            border: 1px solid #efe4db;
            margin-bottom: 32px;
            animation: fadeSlide 1s 0.8s both;
            transition: box-shadow 0.3s ease;
        }

        .details:hover {
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.03);
        }

        .details-row {
            display: flex;
            align-items: flex-start;
            gap: 16px;
            padding: 12px 0;
            border-bottom: 1px solid #eee5dd;
            transition: background 0.2s ease, padding-left 0.2s ease;
            border-radius: 8px;
        }

        .details-row:hover {
            background: rgba(255, 255, 255, 0.3);
            padding-left: 6px;
        }

        .details-row:last-child {
            border-bottom: none;
        }

        .details-row .icon {
            font-size: 1.5rem;
            width: 32px;
            text-align: center;
            color: #b8a08e;
            flex-shrink: 0;
            animation: floatIcon 4s ease-in-out infinite alternate;
        }

        .details-row:nth-child(2) .icon { animation-delay: 0.5s; }
        .details-row:nth-child(3) .icon { animation-delay: 1s; }
        .details-row:nth-child(4) .icon { animation-delay: 1.5s; }

        @keyframes floatIcon {
            0% { transform: translateY(0) rotate(0deg); }
            100% { transform: translateY(-5px) rotate(3deg); }
        }

        .details-row .info {
            font-size: 0.95rem;
            line-height: 1.5;
            color: #3d3630;
        }

        .details-row .info strong {
            font-weight: 600;
            display: block;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: #b09886;
            margin-bottom: 2px;
        }

        .details-row .info .address {
            font-weight: 300;
            font-size: 0.9rem;
            color: #5f554a;
        }

        .details-row .info a {
            color: #8a7a6b;
            text-decoration: none;
            border-bottom: 1px dashed #d5c8bc;
            transition: color 0.2s, border-color 0.2s;
        }

        .details-row .info a:hover {
            color: #4a3a2e;
            border-bottom-color: #4a3a2e;
        }

        /* ---------- RSVP ---------- */
        .rsvp-section {
            background: rgba(243, 236, 229, 0.6);
            backdrop-filter: blur(4px);
            border-radius: 24px;
            padding: 28px 24px 24px;
            margin-bottom: 20px;
            animation: fadeSlide 1s 0.9s both;
            transition: background 0.4s ease, box-shadow 0.3s ease;
            border: 1px solid #efe4db;
        }

        .rsvp-section:hover {
            background: rgba(243, 236, 229, 0.8);
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.03);
        }

        .rsvp-section h3 {
            font-family: 'Great Vibes', cursive;
            font-size: 2rem;
            font-weight: 400;
            color: #4a3a2e;
            text-align: center;
            margin-bottom: 18px;
            animation: fadeSlide 1s 1s both;
        }

        .rsvp-form {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .rsvp-form .form-row {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .rsvp-form .form-row input,
        .rsvp-form .form-row select {
            flex: 1;
            min-width: 130px;
            padding: 14px 16px;
            border: 1px solid #ddd0c4;
            border-radius: 16px;
            font-family: 'Inter', sans-serif;
            font-size: 0.9rem;
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(2px);
            color: #2d2a24;
            outline: none;
            transition: border 0.3s, box-shadow 0.3s, transform 0.2s, background 0.3s;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.01);
        }

        .rsvp-form .form-row input:focus,
        .rsvp-form .form-row select:focus {
            border-color: #b09886;
            box-shadow: 0 0 0 4px rgba(176, 152, 134, 0.15);
            background: #fff;
            transform: scale(1.01);
        }

        .rsvp-form .form-row input:hover,
        .rsvp-form .form-row select:hover {
            border-color: #c5b5a8;
        }

        .rsvp-form .form-row input::placeholder {
            color: #b8a8a0;
            font-weight: 300;
        }

        .rsvp-form button {
            width: 100%;
            padding: 16px;
            border: none;
            border-radius: 18px;
            background: #4a3a2e;
            color: #fff;
            font-family: 'Inter', sans-serif;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 0.5px;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s, box-shadow 0.3s;
            margin-top: 4px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(74, 58, 46, 0.15);
        }

        .rsvp-form button::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, transparent 60%);
            opacity: 0;
            transition: opacity 0.4s;
            transform: rotate(25deg);
        }

        .rsvp-form button:hover {
            background: #5f4c3d;
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(74, 58, 46, 0.2);
        }

        .rsvp-form button:hover::after {
            opacity: 1;
        }

        .rsvp-form button:active {
            transform: scale(0.97);
            box-shadow: 0 2px 8px rgba(74, 58, 46, 0.1);
        }

        .rsvp-message {
            text-align: center;
            font-size: 0.95rem;
            font-weight: 400;
            color: #4a7a5a;
            margin-top: 16px;
            min-height: 28px;
            transition: opacity 0.4s ease, transform 0.3s ease;
            padding: 6px 0;
            border-radius: 12px;
        }

        .rsvp-message.error {
            color: #b15a4a;
            background: rgba(177, 90, 74, 0.06);
        }

        .rsvp-message.success {
            color: #3d7a5a;
            background: rgba(61, 122, 90, 0.06);
        }

        /* ---------- FOOTER ---------- */
        .footer {
            text-align: center;
            padding: 20px 28px 26px;
            border-top: 1px solid #efe4db;
            font-size: 0.8rem;
            color: #b8a8a0;
            letter-spacing: 0.5px;
            background: rgba(252, 250, 248, 0.7);
            backdrop-filter: blur(4px);
            border-radius: 0 0 36px 36px;
            animation: fadeSlide 1s 1.1s both;
        }

        .footer .hearts {
            font-size: 1.4rem;
            letter-spacing: 6px;
            color: #d9c8bc;
            margin-bottom: 4px;
            animation: heartPulse 2s ease-in-out infinite;
        }

        @keyframes heartPulse {
            0%, 100% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.1); opacity: 1; }
        }

        .footer span {
            display: inline-block;
        }

        /* ---------- RESPONSIVE ---------- */
        @media (max-width: 520px) {
            .hero h1 { font-size: 2.8rem; }
            .countdown-item { min-width: 62px; padding: 10px 6px; }
            .countdown-item .number { font-size: 1.8rem; }
            .details-row { flex-direction: column; gap: 4px; padding: 14px 0; }
            .details-row .icon { width: auto; text-align: left; }
            .rsvp-form .form-row { flex-direction: column; }
            .rsvp-form .form-row input,
            .rsvp-form .form-row select { min-width: auto; }
            .content { padding: 30px 18px 24px; }
            .hero { padding: 30px 18px 26px; }
            .card { border-radius: 32px; }
        }

        @media (max-width: 380px) {
            .hero h1 { font-size: 2.2rem; }
            .countdown { gap: 6px; }
            .countdown-item { min-width: 50px; padding: 8px 4px; }
            .countdown-item .number { font-size: 1.4rem; }
            .rsvp-section h3 { font-size: 1.6rem; }
        }

        /* ---------- ANIMATIONS DE CHARGEMENT ---------- */
        .load-delay-1 { animation-delay: 0.2s; }
        .load-delay-2 { animation-delay: 0.4s; }
        .load-delay-3 { animation-delay: 0.6s; }
        .load-delay-4 { animation-delay: 0.8s; }
        .load-delay-5 { animation-delay: 1.0s; }
        .load-delay-6 { animation-delay: 1.2s; }

        /* Effet de brillance sur le titre */
        .shimmer {
            background: linear-gradient(120deg, #4a3a2e 0%, #b8a08e 30%, #4a3a2e 60%, #b8a08e 90%, #4a3a2e 100%);
            background-size: 200% 100%;
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: shimmerText 6s linear infinite;
        }

        @keyframes shimmerText {
            0% { background-position: -200% 0; }
            100% { background-position: 200% 0; }
        }
    </style>
</head>
<body>

    <div class="card" role="main" aria-label="Invitation au mariage de Julie et Antoine">

        <!-- ====== HERO ====== -->
        <div class="hero">
            <!-- décoration florale animée -->
            <div class="hero-bg-decoration">
                <span>🌸</span>
                <span>🌷</span>
                <span>🌹</span>
                <span>🌺</span>
            </div>

            <div class="floral-icon">✿ ✿ ✿</div>
            <h1 class="shimmer">Julie &amp; Antoine</h1>
            <di            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 24px;
            background-image: radial-gradient(circle at 10% 30%, rgba(235, 215, 195, 0.3) 0%, transparent 60%),
                radial-gradient(circle at 90% 70%, rgba(210, 180, 160, 0.2) 0%, transparent 50%);
        }

        .card {
            max-width: 580px;
            width: 100%;
            background: #ffffff;
            border-radius: 40px 40px 32px 32px;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.08), 0 10px 30px rgba(0, 0, 0, 0.04);
            overflow: hidden;
            transition: transform 0.3s ease;
            position: relative;
        }

        .card:hover {
            transform: translateY(-4px);
        }

        /* ---------- HERO / FLORAL TOP ---------- */
        .hero {
            background: linear-gradient(145deg, #f9f0e8, #f3e6db);
            padding: 36px 28px 28px;
            text-align: center;
            position: relative;
            border-bottom: 2px solid #e8d7cc;
        }

        .hero::after {
            content: "✦ ✦ ✦";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            background: #fff;
            padding: 0 16px;
            font-size: 14px;
            letter-spacing: 6px;
            color: #b8a08e;
        }

        .floral-icon {
            font-size: 28px;
            letter-spacing: 6px;
            color: #b8a08e;
            margin-bottom: 8px;
        }

        .hero h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 3.2rem;
            font-weight: 400;
            color: #4a3a2e;
            line-height: 1.1;
            margin-bottom: 4px;
        }

        .hero .and {
            font-family: 'Inter', sans-serif;
            font-weight: 300;
            font-size: 1rem;
            letter-spacing: 4px;
            text-transform: uppercase;
            color: #b09886;
            margin: 4px 0 6px;
        }

        .hero .date-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            backdrop-filter: blur(4px);
            padding: 8px 24px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            color: #4a3a2e;
            border: 1px solid rgba(255, 255, 255, 0.8);
            margin-top: 10px;
            letter-spacing: 0.5px;
        }

        .hero .date-badge span {
            font-weight: 300;
            color: #b09886;
        }

        /* ---------- CONTENT ---------- */
        .content {
            padding: 36px 28px 32px;
        }

        .message {
            text-align: center;
            font-weight: 300;
            font-size: 1rem;
            line-height: 1.7;
            color: #4a3f38;
            margin-bottom: 28px;
        }

        .message strong {
            font-weight: 600;
            color: #2d2a24;
        }

        /* ---------- COUNTDOWN ---------- */
        .countdown {
            display: flex;
            justify-content: center;
            gap: 12px;
            margin-bottom: 32px;
            flex-wrap: wrap;
        }

        .countdown-item {
            background: #f9f3ee;
            border-radius: 16px;
            padding: 12px 10px;
            min-width: 68px;
            text-align: center;
            border: 1px solid #efe4db;
            flex: 1 0 auto;
        }

        .countdown-item .number {
            font-family: 'Inter', sans-serif;
            font-size: 2rem;
            font-weight: 600;
            color: #4a3a2e;
            display: block;
            line-height: 1.2;
            letter-spacing: -0.5px;
        }

        .countdown-item .label {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: #b09886;
            font-weight: 400;
            margin-top: 2px;
        }

        /* ---------- DETAILS ---------- */
        .details {
            background: #fcf8f4;
            border-radius: 20px;
            padding: 20px 22px;
            border: 1px solid #efe4db;
            margin-bottom: 30px;
        }

        .details-row {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            padding: 10px 0;
            border-bottom: 1px solid #eee5dd;
        }

        .details-row:last-child {
            border-bottom: none;
        }

        .details-row .icon {
            font-size: 1.3rem;
            width: 28px;
            text-align: center;
            color: #b8a08e;
            flex-shrink: 0;
        }

        .details-row .info {
            font-size: 0.95rem;
            line-height: 1.5;
            color: #3d3630;
        }

        .details-row .info strong {
            font-weight: 600;
            display: block;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #b09886;
            margin-bottom: 1px;
        }

        .details-row .info .address {
            font-weight: 300;
            font-size: 0.9rem;
            color: #5f554a;
        }

        .details-row .info a {
            color: #8a7a6b;
            text-decoration: none;
            border-bottom: 1px dashed #d5c8bc;
            transition: color 0.2s;
        }

        .details-row .info a:hover {
            color: #4a3a2e;
            border-bottom-color: #4a3a2e;
        }

        /* ---------- RSVP ---------- */
        .rsvp-section {
            background: #f3ece5;
            border-radius: 20px;
            padding: 24px 22px 22px;
            margin-bottom: 20px;
            transition: background 0.3s;
        }

        .rsvp-section h3 {
            font-family: 'Great Vibes', cursive;
            font-size: 1.8rem;
            font-weight: 400;
            color: #4a3a2e;
            text-align: center;
            margin-bottom: 14px;
        }

        .rsvp-form {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .rsvp-form .form-row {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .rsvp-form .form-row input,
        .rsvp-form .form-row select {
            flex: 1;
            min-width: 120px;
            padding: 12px 14px;
            border: 1px solid #ddd0c4;
            border-radius: 12px;
            font-family: 'Inter', sans-serif;
            font-size: 0.9rem;
            background: #fff;
            color: #2d2a24;
            outline: none;
            transition: border 0.25s, box-shadow 0.25s;
        }

        .rsvp-form .form-row input:focus,
        .rsvp-form .form-row select:focus {
            border-color: #b09886;
            box-shadow: 0 0 0 3px rgba(176, 152, 134, 0.15);
        }

        .rsvp-form .form-row input::placeholder {
            color: #b8a8a0;
            font-weight: 300;
        }

        .rsvp-form button {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 14px;
            background: #4a3a2e;
            color: #fff;
            font-family: 'Inter', sans-serif;
            font-weight: 600;
            font-size: 0.95rem;
            letter-spacing: 0.5px;
            cursor: pointer;
            transition: background 0.25s, transform 0.15s;
            margin-top: 4px;
        }

        .rsvp-form button:hover {
            background: #5f4c3d;
        }

        .rsvp-form button:active {
            transform: scale(0.97);
        }

        .rsvp-message {
            text-align: center;
            font-size: 0.9rem;
            font-weight: 400;
            color: #4a7a5a;
            margin-top: 12px;
            min-height: 26px;
            transition: opacity 0.3s;
        }

        .rsvp-message.error {
            color: #b15a4a;
        }

        /* ---------- FOOTER ---------- */
        .footer {
            text-align: center;
            padding: 18px 28px 24px;
            border-top: 1px solid #efe4db;
            font-size: 0.8rem;
            color: #b8a8a0;
            letter-spacing: 0.5px;
            background: #fcfaf8;
            border-radius: 0 0 32px 32px;
        }

        .footer .hearts {
            font-size: 1.2rem;
            letter-spacing: 4px;
            color: #d9c8bc;
            margin-bottom: 4px;
        }

        /* ---------- RESPONSIVE ---------- */
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.6rem;
            }
            .countdown-item {
                min-width: 58px;
                padding: 10px 6px;
            }
            .countdown-item .number {
                font-size: 1.6rem;
            }
            .details-row {
                flex-direction: column;
                gap: 4px;
                padding: 12px 0;
            }
            .details-row .icon {
                width: auto;
                text-align: left;
            }
            .rsvp-form .form-row {
                flex-direction: column;
            }
            .rsvp-form .form-row input,
            .rsvp-form .form-row select {
                min-width: auto;
            }
        }

        @media (max-width: 380px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            .countdown {
                gap: 6px;
            }
            .countdown-item {
                min-width: 48px;
                padding: 8px 4px;
            }
            .countdown-item .number {
                font-size: 1.3rem;
            }
        }

        /* ---------- UTILITY ---------- */
        .hidden {
            display: none !important;
        }
    </style>
</head>
<body>

    <div class="card" role="main" aria-label="Invitation au mariage de Julie et Antoine">

        <!-- ====== HERO ====== -->
        <div class="hero">
            <div class="floral-icon">✿ ✿ ✿</div>
            <h1>Julie &amp; Antoine</h1>
            <div class="and">— s'unissent —</div>
            <div class="date-badge">
                <span>📅</span> 26 Juillet 2026 <span>·</span> 16h00
            </div>
        </div>

        <!-- ====== CONTENT ====== -->
        <div class="content">

            <!-- Message -->
            <p class="message">
                Nous avons le plaisir de vous inviter à partager
                <strong>notre jour le plus précieux</strong>.
                <br />
                Votre présence nous comblera de bonheur.
            </p>

            <!-- Countdown -->
            <div class="countdown" id="countdown" aria-label="Compte à rebours jusqu'au mariage">
                <div class="countdown-item">
                    <span class="number" id="days">--</span>
                    <span class="label">Jours</span>
                </div>
                <div class="countdown-item">
                    <span class="number" id="hours">--</span>
                    <span class="label">Heures</span>
                </div>
                <div class="countdown-item">
                    <span class="number" id="minutes">--</span>
                    <span class="label">Minutes</span>
                </div>
                <div class="countdown-item">
                    <span class="number" id="seconds">--</span>
                    <span class="label">Secondes</span>
                </div>
            </div>

            <!-- Détails -->
            <div class="details">
                <div class="details-row">
                    <span class="icon">📍</span>
                    <div class="info">
                        <strong>Lieu</strong>
                        <span class="address">Domaine de la Roseraie · 42 route des Vignes, 33200 Bordeaux</span>
                    </div>
                </div>
                <div class="details-row">
                    <span class="icon">🕊️</span>
                    <div class="info">
                        <strong>Cérémonie</strong>
                        <span>16h00 · Jardin d'honneur <br /><span style="font-size:0.8rem; color:#b09886;">(suivie du cocktail et du dîner)</span></span>
                    </div>
                </div>
                <div class="details-row">
                    <span class="icon">👗</span>
                    <div class="info">
                        <strong>Code vestimentaire</strong>
                        <span>Élégant · Tenue de soirée</span>
                    </div>
                </div>
                <div class="details-row">
                    <span class="icon">📋</span>
                    <div class="info">
                        <strong>Réponse souhaitée avant le</strong>
                        <span>15 Juin 2026</span>
                    </div>
                </div>
            </div>

            <!-- RSVP -->
            <div class="rsvp-section" id="rsvpSection">
                <h3>Confirmez votre présence</h3>
                <form class="rsvp-form" id="rsvpForm" novalidate>
                    <div class="form-row">
                        <input type="text" id="rsvpName" placeholder="Votre nom & prénom" required />
                        <input type="email" id="rsvpEmail" placeholder="Email" required />
                    </div>
                    <div class="form-row">
                        <select id="rsvpGuests" required>
                            <option value="">Nombre de personnes</option>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                            <option value="4">4</option>
                        </select>
                        <select id="rsvpStatus" required>
                            <option value="">Présence</option>
                            <option value="yes">✅ Oui, je viens</option>
                            <option value="no">❌ Non, je ne peux pas</option>
                        </select>
                    </div>
                    <button type="submit" id="rsvpBtn">💌 Envoyer ma réponse</button>
                </form>
                <div class="rsvp-message" id="rsvpMessage"></div>
            </div>

        </div>

        <!-- ====== FOOTER ====== -->
        <div class="footer">
            <div class="hearts">♥ ♥ ♥</div>
            <span>Julie &amp; Antoine · 26.07.2026</span>
            <br />
            <span style="font-size:0.7rem; color:#ccc5bd;">#JulieAntoine2026</span>
        </div>

    </div>

    <script>
        (function() {
            'use strict';

            // ============================================================
            // 1. COUNTDOWN
            // ============================================================
            const WEDDING_DATE = new Date('July 26, 2026 16:00:00').getTime();

            const daysEl = document.getElementById('days');
            const hoursEl = document.getElementById('hours');
            const minutesEl = document.getElementById('minutes');
            const secondsEl = document.getElementById('seconds');

            function updateCountdown() {
                const now = Date.now();
                let diff = WEDDING_DATE - now;

                if (diff < 0) diff = 0;

                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((diff % (1000 * 60)) / 1000);

                daysEl.textContent = String(days).padStart(2, '0');
                hoursEl.textContent = String(hours).padStart(2, '0');
                minutesEl.textContent = String(minutes).padStart(2, '0');
                secondsEl.textContent = String(seconds).padStart(2, '0');
            }

            updateCountdown();
            const countdownInterval = setInterval(updateCountdown, 1000);

            // ============================================================
            // 2. RSVP FORM
            // ============================================================
            const form = document.getElementById('rsvpForm');
            const messageEl = document.getElementById('rsvpMessage');

            function showMessage(text, isError = false) {
                messageEl.textContent = text;
                messageEl.className = 'rsvp-message' + (isError ? ' error' : '');
            }

            form.addEventListener('submit', function(e) {
                e.preventDefault();

                const name = document.getElementById('rsvpName').value.trim();
                const email = document.getElementById('rsvpEmail').value.trim();
                const guests = document.getElementById('rsvpGuests').value;
                const status = document.getElementById('rsvpStatus').value;

                // Validation basique
                if (!name || name.length < 2) {
                    showMessage('Veuillez indiquer votre nom et prénom.', true);
                    return;
                }
                if (!email || !email.includes('@') || !email.includes('.')) {
                    showMessage('Veuillez entrer une adresse email valide.', true);
                    return;
                }
                if (!guests) {
                    showMessage('Précisez le nombre de personnes.', true);
                    return;
                }
                if (!status) {
                    showMessage('Choisissez votre statut de présence.', true);
                    return;
                }

                // Simuler un envoi réussi
                const statusLabel = status === 'yes' ? '✅ présent(e)' : '❌ absent(e)';
                const guestLabel = guests === '1' ? '1 personne' : guests + ' personnes';

                showMessage(
                    `✅ Merci ${name} ! Votre réponse (${statusLabel}, ${guestLabel}) a bien été enregistrée.`,
                    false
                );

                // Réinitialiser le formulaire après un délai (ou on laisse l'utilisateur le faire)
                // On désactive les champs pour éviter les doubles envois
                form.querySelectorAll('input, select, button').forEach(el => el.disabled = true);
                document.getElementById('rsvpBtn').textContent = '✓ Réponse envoyée';

                // Optionnel : réactiver après 10s (pour démonstration)
                setTimeout(() => {
                    form.querySelectorAll('input, select, button').forEach(el => el.disabled = false);
                    document.getElementById('rsvpBtn').textContent = '💌 Envoyer ma réponse';
                    // On ne réinitialise pas les champs pour que l'utilisateur puisse modifier
                }, 10000);
            });

            // ============================================================
            // 3. NETTOYAGE (bonne pratique)
            // =====================================================
