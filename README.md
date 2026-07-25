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
            // =====================================================
