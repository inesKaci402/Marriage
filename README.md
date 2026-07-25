<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>💍 Invitation Mariage - Julie & Antoine</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600&display=swap" rel="stylesheet" />
    <style>
        /* ---------- RESET & BASE ---------- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #faf6f0;
            color: #2d2a24;
            display: flex;
            justify-content: center;
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
            // =====================================================            justify-content: center;
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
            // =====================================================            align-items: center;
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
            <di    font-family:'Jost', sans-serif;
    overflow-x:hidden;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.serif{font-family:'Cormorant Garamond', serif;font-weight:500;}

  canvas#petals{
    position:fixed;
    inset:0;
    z-index:60;
    pointer-events:none;
  }

  /* ================= Enveloppe ================= */
  #envelope-screen{
    position:fixed;inset:0;
    background:radial-gradient(ellipse at 50% 30%, #3f4e30 0%, #2c351f 75%);
    display:flex;align-items:center;justify-content:center;
    z-index:100;
    transition:opacity 1s ease, visibility 1s ease;
  }
  #envelope-screen.hidden{opacity:0;visibility:hidden;pointer-events:none;}
  .envelope-wrap{text-align:center;color:var(--ivory);}
  .envelope-names{
    font-size:1.7rem;letter-spacing:.06em;margin-bottom:.8rem;opacity:0;
    animation:fadeInDown 1s ease forwards .2s;
  }
  .envelope{
    position:relative;width:260px;height:180px;margin:0 auto 2.2rem;cursor:pointer;
    opacity:0;
    animation:popIn .8s cubic-bezier(.34,1.56,.64,1) forwards .5s;
  }
  .env-body{
    position:absolute;inset:0;background:#EDE6D6;border-radius:4px;
    box-shadow:0 20px 45px rgba(0,0,0,0.45);
  }
  .env-flap{
    position:absolute;top:0;left:0;right:0;height:0;
    border-left:130px solid transparent;border-right:130px solid transparent;
    border-top:100px solid #DCD2B8;
    transform-origin:top center;
    transition:transform 1.1s cubic-bezier(.6,.2,.2,1);
    z-index:3;
  }
  .envelope.open .env-flap{transform:rotateX(180deg);}
  .seal{
    position:absolute;top:78px;left:50%;transform:translate(-50%,0);
    width:46px;height:46px;background:var(--rose);border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    font-family:'Cormorant Garamond',serif;font-size:1.3rem;color:var(--ivory);
    box-shadow:0 3px 8px rgba(0,0,0,0.35);z-index:4;
    transition:opacity .4s ease, transform .4s ease;
    animation:pulseSeal 2s ease-in-out infinite;
  }
  .envelope.open .seal{opacity:0;transform:translate(-50%,0) scale(.4);animation:none;}
  .env-letter{
    position:absolute;left:14px;right:14px;top:14px;height:150px;
    background:var(--ivory);border-radius:2px;box-shadow:0 4px 10px rgba(0,0,0,0.2);
    z-index:2;transition:transform 1s cubic-bezier(.5,0,.2,1) .15s;
    display:flex;align-items:center;justify-content:center;
    font-family:'Cormorant Garamond',serif;letter-spacing:.08em;color:var(--olive);
    font-size:.95rem;text-transform:uppercase;
  }
  .envelope.open .env-letter{transform:translateY(-190px);}
  .envelope-hint{
    font-size:.78rem;letter-spacing:.18em;text-transform:uppercase;color:var(--rose);
    opacity:0;animation:fadeInDown 1s ease forwards .9s;
  }

  @keyframes popIn{from{opacity:0;transform:scale(.85);}to{opacity:1;transform:scale(1);}}
  @keyframes fadeInDown{from{opacity:0;transform:translateY(-10px);}to{opacity:1;transform:translateY(0);}}
  @keyframes pulseSeal{0%,100%{box-shadow:0 3px 8px rgba(0,0,0,.35), 0 0 0 0 rgba(201,139,122,.5);}50%{box-shadow:0 3px 8px rgba(0,0,0,.35), 0 0 0 10px rgba(201,139,122,0);}}

  /* ================= Structure ================= */
  section{padding:6rem 1.5rem;position:relative;overflow:hidden;}
  .container{max-width:760px;margin:0 auto;position:relative;z-index:2;}
  .center{text-align:center;}
  .eyebrow{
    font-size:.72rem;letter-spacing:.32em;text-transform:uppercase;color:var(--rose);
    margin-bottom:1rem;
  }
  .branch-divider{width:120px;height:24px;margin:1.6rem auto;opacity:.75;}

  .fade-up{opacity:0;transform:translateY(28px);transition:opacity .9s ease, transform .9s ease;}
  .fade-up.in{opacity:1;transform:translateY(0);}
  .fade-up.d1.in{transition-delay:.1s;}
  .fade-up.d2.in{transition-delay:.22s;}
  .fade-up.d3.in{transition-delay:.34s;}
  .fade-up.d4.in{transition-delay:.46s;}

  .scale-in{opacity:0;transform:scale(.88);transition:opacity .8s ease, transform .8s cubic-bezier(.34,1.2,.64,1);}
  .scale-in.in{opacity:1;transform:scale(1);}

  /* ================= Hero ================= */
  #hero{
    min-height:100vh;
    display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;
    background:var(--ivory);
    opacity:0;transform:translateY(14px);
    transition:opacity 1.1s ease .2s, transform 1.1s ease .2s;
  }
  #hero.reveal{opacity:1;transform:translateY(0);}

  .hero-bg-blob{
    position:absolute;border-radius:50%;filter:blur(60px);z-index:0;
    animation:float 9s ease-in-out infinite;
  }
  .blob1{width:340px;height:340px;background:rgba(74,93,58,0.14);top:-8%;left:-10%;}
  .blob2{width:280px;height:280px;background:rgba(201,139,122,0.16);bottom:-6%;right:-8%;animation-delay:2s;}
  @keyframes float{
    0%,100%{transform:translate(0,0) scale(1);}
    50%{transform:translate(18px,-22px) scale(1.06);}
  }

  .photo-frame{
    width:168px;height:168px;
    border-radius:50%;
    border:2px solid var(--gold);
    position:relative;z-index:2;
    margin-bottom:1.8rem;
    display:flex;align-items:center;justify-content:center;
    cursor:pointer;
    overflow:hidden;
    background:
      linear-gradient(135deg, #EFE8D8, #E3DAC4);
    transition:transform .35s ease, box-shadow .35s ease;
    box-shadow:0 10px 30px rgba(74,93,58,0.18);
  }
  .photo-frame:hover{transform:translateY(-4px) scale(1.03);box-shadow:0 16px 36px rgba(74,93,58,0.26);}
  .photo-frame img{width:100%;height:100%;object-fit:cover;}
  .photo-frame .ph-placeholder{
    display:flex;flex-direction:column;align-items:center;gap:.4rem;color:var(--olive-dark);
    padding:0 1rem;text-align:center;
  }
  .photo-frame .ph-placeholder svg{width:30px;height:30px;opacity:.6;}
  .photo-frame .ph-placeholder span{font-size:.62rem;letter-spacing:.1em;text-transform:uppercase;opacity:.75;}
  .photo-frame input[type=file]{display:none;}

  .hero-eyebrow{
    font-size:.75rem;letter-spacing:.35em;text-transform:uppercase;color:var(--olive);
    margin-bottom:1.4rem;position:relative;z-index:2;
  }
  .hero-names{font-size:clamp(3rem, 10vw, 6rem);line-height:1.05;color:var(--ink);position:relative;z-index:2;}
  .hero-amp{display:block;font-style:italic;color:var(--rose);font-size:clamp(2rem, 6vw, 3.2rem);margin:.2rem 0;}
  .hero-date{margin-top:1.8rem;font-size:1rem;letter-spacing:.22em;text-transform:uppercase;color:var(--olive-dark);position:relative;z-index:2;}
  .hero-place{margin-top:.4rem;font-size:.85rem;color:#6b6558;letter-spacing:.05em;position:relative;z-index:2;}

  .scroll-cue{
    position:absolute;bottom:2.2rem;left:50%;transform:translateX(-50%);
    display:flex;flex-direction:column;align-items:center;gap:.4rem;
    color:var(--olive);opacity:.7;z-index:2;
    animation:bounce 2s ease-in-out infinite;
  }
  .scroll-cue span{font-size:.62rem;letter-spacing:.18em;text-transform:uppercase;}
  @keyframes bounce{0%,100%{transform:translate(-50%,0);}50%{transform:translate(-50%,8px);}}

  /* ================= Compte à rebours ================= */
  #countdown{background:var(--olive);color:var(--ivory);}
  .countdown-title{font-size:1.7rem;margin-bottom:2.4rem;text-align:center;}
  .countdown-grid{display:flex;justify-content:center;gap:1.2rem;flex-wrap:wrap;}
  .cd-item{
    min-width:90px;text-align:center;padding:0;
    perspective:600px;
  }
  .cd-flip{
    background:rgba(251,247,238,0.06);
    border:1px solid rgba(251,247,238,0.25);
    border-radius:8px;
    padding:1.4rem .6rem 1.1rem;
  }
  .cd-num{
    font-family:'Cormorant Garamond',serif;font-size:2.7rem;line-height:1;
    display:inline-block;
    transition:transform .3s ease;
  }
  .cd-num.tick{animation:tick .4s ease;}
  @keyframes tick{
    0%{transform:translateY(0);opacity:1;}
    40%{transform:translateY(-8px);opacity:.3;}
    41%{transform:translateY(8px);}
    100%{transform:translateY(0);opacity:1;}
  }
  .cd-label{margin-top:.5rem;font-size:.66rem;letter-spacing:.16em;text-transform:uppercase;color:var(--rose-light);}

  /* ================= Notre histoire ================= */
  .story-grid{display:grid;gap:3rem;margin-top:3rem;}
  .story-item{
    display:grid;grid-template-columns:96px 1fr;gap:1.6rem;align-items:center;
  }
  .story-item:nth-child(even){grid-template-columns:1fr 96px;}
  .story-item:nth-child(even) .story-photo{order:2;}
  .story-item:nth-child(even) .story-text{order:1;text-align:right;}

  .story-photo{
    width:96px;height:96px;border-radius:12px;
    border:2px solid var(--rose-light);
    cursor:pointer;overflow:hidden;position:relative;
    background:linear-gradient(135deg,#EFE8D8,#E3DAC4);
    display:flex;align-items:center;justify-content:center;
    transition:transform .3s ease;
  }
  .story-photo:hover{transform:rotate(-2deg) scale(1.04);}
  .story-photo img{width:100%;height:100%;object-fit:cover;}
  .story-photo svg{width:24px;height:24px;opacity:.55;color:var(--olive-dark);}
  .story-photo input[type=file]{display:none;}

  .story-year{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:1.2rem;color:var(--rose);display:block;margin-bottom:.2rem;}
  .story-text h3{font-size:1.4rem;margin-bottom:.35rem;}
  .story-text p{font-size:.9rem;line-height:1.6;color:#54503f;}

  /* ================= Galerie ================= */
  #gallery{background:#F3EEE1;}
  .gallery-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:1rem;
    margin-top:2.8rem;
  }
  .gallery-item{
    aspect-ratio:1/1;
    border-radius:10px;
    background:linear-gradient(135deg,#EFE8D8,#E3DAC4);
    border:1px solid var(--line);
    cursor:pointer;
    position:relative;overflow:hidden;
    display:flex;align-items:center;justify-content:center;
    transition:transform .35s ease, box-shadow .35s ease;
  }
  .gallery-item:hover{transform:translateY(-5px);box-shadow:0 14px 26px rgba(74,93,58,0.18);}
  .gallery-item img{width:100%;height:100%;object-fit:cover;}
  .gallery-item .gp{display:flex;flex-direction:column;align-items:center;gap:.4rem;color:var(--olive-dark);opacity:.55;}
  .gallery-item .gp svg{width:26px;height:26px;}
  .gallery-item .gp span{font-size:.6rem;letter-spacing:.1em;text-transform:uppercase;}
  .gallery-item input[type=file]{display:none;}

  /* Lightbox */
  #lightbox{
    position:fixed;inset:0;background:rgba(20,18,14,0.92);
    display:none;align-items:center;justify-content:center;z-index:90;
    padding:2rem;
  }
  #lightbox.show{display:flex;animation:fadeIn .3s ease;}
  @keyframes fadeIn{from{opacity:0;}to{opacity:1;}}
  #lightbox img{max-width:min(90vw,600px);max-height:80vh;border-radius:8px;box-shadow:0 20px 50px rgba(0,0,0,.5);}
  #lightbox-close{
    position:absolute;top:1.6rem;right:1.8rem;color:var(--ivory);font-size:1.6rem;
    cursor:pointer;background:none;border:none;
  }

  /* ================= Détails ================= */
  .details-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.8rem;margin-top:2.6rem;}
  .detail-card{
    background:var(--ivory);border:1px solid var(--line);border-radius:8px;
    padding:2rem 1.6rem;text-align:center;
    transition:transform .3s ease, box-shadow .3s ease;
  }
  .detail-card:hover{transform:translateY(-4px);box-shadow:0 14px 26px rgba(74,93,58,0.14);}
  .detail-card h3{font-size:1.5rem;margin-bottom:.6rem;color:var(--olive-dark);}
  .detail-card p{font-size:.85rem;line-height:1.65;color:#54503f;}
  .detail-time{display:inline-block;margin-top:.9rem;font-size:.72rem;letter-spacing:.15em;text-transform:uppercase;color:var(--rose);}

  /* ================= RSVP ================= */
  form{max-width:460px;margin:2.6rem auto 0;display:flex;flex-direction:column;gap:1.2rem;}
  .field{display:flex;flex-direction:column;gap:.4rem;text-align:left;}
  label{font-size:.7rem;letter-spacing:.14em;text-transform:uppercase;color:var(--olive-dark);}
  input[type=text], input[type=email], select{
    font-family:'Jost',sans-serif;font-size:.92rem;padding:.75rem .9rem;
    border:1px solid var(--line);border-radius:4px;background:#fff;color:var(--ink);
    transition:border-color .25s ease, box-shadow .25s ease;
  }
  input:focus, select:focus, button:focus, .photo-frame:focus, .gallery-item:focus, .story-photo:focus, .envelope:focus{
    outline:none;border-color:var(--rose);box-shadow:0 0 0 3px rgba(201,139,122,0.25);
  }
  .guests-row{display:flex;gap:1rem;}
  .guests-row .field{flex:1;}
  button.submit{
    margin-top:.6rem;padding:.95rem 1.4rem;background:var(--olive);color:var(--ivory);
    border:none;border-radius:4px;font-family:'Jost',sans-serif;font-size:.85rem;
    letter-spacing:.14em;text-transform:uppercase;cursor:pointer;
    transition:background .25s ease, transform .25s ease;
  }
  button.submit:hover{background:var(--olive-dark);transform:translateY(-1px);}
  .rsvp-confirm{
    display:none;margin-top:2rem;padding:1.4rem;border:1px solid var(--rose);border-radius:6px;
    text-align:center;color:var(--olive-dark);font-size:.92rem;
  }
  .rsvp-confirm.show{display:block;animation:popIn .5s ease;}

  footer{text-align:center;padding:3rem 1.5rem 4rem;color:#8c8672;font-size:.78rem;letter-spacing:.08em;}

  @media (max-width:600px){
    .details-grid{grid-template-columns:1fr;}
    .story-item, .story-item:nth-child(even){grid-template-columns:64px 1fr;}
    .story-item:nth-child(even) .story-photo{order:0;}
    .story-item:nth-child(even) .story-text{order:0;text-align:left;}
    .story-photo{width:64px;height:64px;}
    .gallery-grid{grid-template-columns:repeat(2,1fr);}
    .cd-item{min-width:70px;}
    .cd-num{font-size:2rem;}
  }

  @media (prefers-reduced-motion: reduce){
    *{transition:none !important;animation:none !important;}
  }
</style>
</head>
<body>

<canvas id="petals"></canvas>

<!-- ================= Écran enveloppe ================= -->
<div id="envelope-screen">
  <div class="envelope-wrap">
    <div class="envelope-names">Amira &amp; Yanis</div>
    <div class="envelope" id="envelope" tabindex="0" role="button" aria-label="Ouvrir l'invitation">
      <div class="env-letter">Vous êtes invités</div>
      <div class="env-flap"></div>
      <div class="env-body"></div>
      <div class="seal">A&nbsp;Y</div>
    </div>
    <div class="envelope-hint">Touchez l'enveloppe pour l'ouvrir</div>
  </div>
</div>

<!-- ================= Hero ================= -->
<section id="hero">
  <div class="hero-bg-blob blob1"></div>
  <div class="hero-bg-blob blob2"></div>

  <div class="hero-eyebrow">Nous nous marions</div>

  <label class="photo-frame" tabindex="0" aria-label="Ajouter la photo du couple">
    <div class="ph-placeholder" id="hero-ph">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><rect x="3" y="5" width="18" height="15" rx="2"/><circle cx="8.5" cy="10.5" r="1.7"/><path d="M21 16l-5-5-4 4-3-3-5 5"/></svg>
      <span>Ajouter la photo</span>
    </div>
    <input type="file" accept="image/*" data-target="hero-ph">
  </label>

  <h1 class="hero-names">
    Amira
    <span class="hero-amp">&amp;</span>
    Yanis
  </h1>
  <svg class="branch-divider" viewBox="0 0 120 24" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M2 12 C 30 4, 90 4, 118 12" stroke="#4A5D3A" stroke-width="1.2"/>
    <circle cx="30" cy="7.5" r="2.4" fill="#C98B7A"/>
    <circle cx="60" cy="5" r="2.8" fill="#4A5D3A"/>
    <circle cx="90" cy="7.5" r="2.4" fill="#C98B7A"/>
  </svg>
  <div class="hero-date">Samedi 12 Septembre 2026</div>
  <div class="hero-place">Domaine des Oliviers — Tiaret, Algérie</div>

  <div class="scroll-cue">
    <span>Découvrir</span>
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M6 9l6 6 6-6"/></svg>
  </div>
</section>

<!-- ================= Compte à rebours ================= -->
<section id="countdown">
  <div class="container fade-up">
    <div class="countdown-title center serif">Il ne reste plus que...</div>
    <div class="countdown-grid" id="countdown-grid">
      <div class="cd-item"><div class="cd-flip"><span class="cd-num" id="cd-days">00</span></div><div class="cd-label">Jours</div></div>
      <div class="cd-item"><div class="cd-flip"><span class="cd-num" id="cd-hours">00</span></div><div class="cd-label">Heures</div></div>
      <div class="cd-item"><div class="cd-flip"><span class="cd-num" id="cd-min">00</span></div><div class="cd-label">Minutes</div></div>
      <div class="cd-item"><div class="cd-flip"><span class="cd-num" id="cd-sec">00</span></div><div class="cd-label">Secondes</div></div>
    </div>
  </div>
</section>

<!-- ================= Notre histoire ================= -->
<section id="story">
  <div class="container">
    <div class="center fade-up">
      <div class="eyebrow">Notre histoire</div>
      <h2 style="font-size:2.2rem;">Le chemin parcouru ensemble</h2>
    </div>
    <div class="story-grid">
      <div class="story-item fade-up d1">
        <label class="story-photo" tabindex="0" aria-label="Ajouter une photo souvenir 2019">
          <svg id="ph-2019" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><rect x="3" y="5" width="18" height="15" rx="2"/><circle cx="8.5" cy="10.5" r="1.7"/><path d="M21 16l-5-5-4 4-3-3-5 5"/></svg>
          <input type="file" accept="image/*" data-target="ph-2019">
        </label>
        <div class="story-text">
          <span class="story-year">2019</span>
          <h3>Première rencontre</h3>
          <p>Une présentation par des amis communs lors d'un mariage, et une conversation qui ne s'est plus jamais arrêtée.</p>
        </div>
      </div>
      <div class="story-item fade-up d2">
        <label class="story-photo" tabindex="0" aria-label="Ajouter une photo souvenir 2022">
          <svg id="ph-2022" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><rect x="3" y="5" width="18" height="15" rx="2"/><circle cx="8.5" cy="10.5" r="1.7"/><path d="M21 16l-5-5-4 4-3-3-5 5"/></svg>
          <input type="file" accept="image/*" data-target="ph-2022">
        </label>
        <div class="story-text">
          <span class="story-year">2022</span>
          <h3>Emménagement</h3>
          <p>Un petit appartement, beaucoup de cartons, et la certitude tranquille que c'était la bonne décision.</p>
        </div>
      </div>
      <div class="story-item fade-up d3">
        <label class="story-photo" tabindex="0" aria-label="Ajouter une photo souvenir 2025">
          <svg id="ph-2025" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><rect x="3" y="5" width="18" height="15" rx="2"/><circle cx="8.5" cy="10.5" r="1.7"/><path d="M21 16l-5-5-4 4-3-3-5 5"/></svg>
          <input type="file" accept="image/*" data-target="ph-2025">
        </label>
        <div class="story-text">
          <span class="story-year">2025</span>
          <h3>La demande</h3>
          <p>Sur la terrasse, au coucher du soleil, sans discours préparé — juste une question, et un oui immédiat.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ================= Galerie ================= -->
<section id="gallery">
  <div class="container">
    <div class="center fade-up">
      <div class="eyebrow">En images</div>
      <h2 style="font-size:2.2rem;">Notre album</h2>
    </div>
    <div class="gallery-grid" id="gallery-grid">
      <!-- 6 emplacements générés            justify-content: center;
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
