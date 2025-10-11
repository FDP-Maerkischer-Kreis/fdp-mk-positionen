<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FDP Märkischer Kreis - Unsere Positionen</title>
    <meta name="description" content="Entdecken Sie die politischen Positionen der FDP Märkischer Kreis zu wichtigen Themen - interaktiv und übersichtlich dargestellt.">
    <meta name="keywords" content="FDP, Märkischer Kreis, Politik, Positionen, Standpunkte, Liberal, Demokratisch">
    <meta name="author" content="FDP Märkischer Kreis">
    
    <!-- EU-Konformität und SEO -->
    <meta name="robots" content="index, follow">
    <meta name="language" content="DE">
    <link rel="canonical" href="#">
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='%23FFD700'><text y='18' font-size='18'>🔹</text></svg>">
    
    <style>
        /* CSS Reset und Basis-Styling */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --fdp-magenta: #E2007E;
            --fdp-yellow: #FFD700;
            --fdp-blue: #0066CC;
            --fdp-dark: #1a1a1a;
            --fdp-light: #f8f9fa;
            --shadow-light: rgba(0,0,0,0.1);
            --shadow-medium: rgba(0,0,0,0.15);
            --shadow-strong: rgba(0,0,0,0.25);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            padding: 20px;
            color: var(--fdp-dark);
            line-height: 1.6;
        }
        
        /* Header */
        .header {
            text-align: center;
            margin-bottom: 3rem;
            animation: fadeInDown 0.8s ease-out;
        }
        
        .fdp-logo {
            max-width: 400px;
            width: 100%;
            height: auto;
            margin-bottom: 2rem;
            filter: drop-shadow(0 4px 12px var(--shadow-medium)) brightness(0) invert(1);
            transition: var(--transition);
            background: linear-gradient(135deg, var(--fdp-magenta) 0%, #c91565 100%);
            padding: 1.5rem 2rem;
            border-radius: 20px;
            border: 2px solid var(--fdp-yellow);
        }
        
        .fdp-logo:hover {
            transform: scale(1.02);
            filter: drop-shadow(0 6px 16px var(--shadow-strong)) brightness(0) invert(1);
            background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
            border-color: var(--fdp-magenta);
        }
        
        /* Alternative Logo-Container */
        .logo-container {
            display: inline-block;
            margin-bottom: 2rem;
            transition: var(--transition);
            background: transparent;
        }
        
        .logo-container:hover {
            transform: scale(1.02);
        }
        
        .logo-container:hover .original-logo {
            transform: translateY(-5px);
            filter: drop-shadow(0 10px 20px var(--shadow-medium));
            box-shadow: 0 12px 30px var(--shadow-medium);
            background: #ffffff;
        }
        
        .original-logo {
            display: block;
            max-width: 300px;
            width: 100%;
            height: auto;
            /* Einheitlicher weißer Hintergrund ohne Gradient */
            background: #ffffff;
            padding: 1.5rem 2rem;
            border-radius: 15px;
            border: 2px solid var(--fdp-magenta);
            box-shadow: 0 8px 25px var(--shadow-light);
            filter: drop-shadow(0 4px 12px var(--shadow-medium));
            transition: var(--transition);
        }
        
        .header h1 {
            font-size: 2.5rem;
            color: var(--fdp-magenta);
            margin-bottom: 0.5rem;
            font-weight: 700;
            text-shadow: 2px 2px 4px var(--shadow-light);
        }
        
        .header p {
            font-size: 1.1rem;
            color: var(--fdp-dark);
            opacity: 0.8;
            max-width: 600px;
            margin: 0 auto;
        }
        
        /* Grid Container für die Karten */
        .positions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
            padding: 1rem;
        }
        
        /* Flip-Karte Container */
        .flip-card {
            background-color: transparent;
            width: 100%;
            height: 300px;
            perspective: 1000px;
            border-radius: 15px;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s ease-out, filter 0.3s ease-out;
        }
        
        .flip-card:hover {
            transform: translateY(-5px);
            filter: drop-shadow(0 10px 20px var(--shadow-medium));
        }
        
        .flip-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            transform-style: preserve-3d;
            border-radius: 15px;
        }
        
        .flip-card:hover .flip-card-inner,
        .flip-card.flipped .flip-card-inner {
            transform: rotateY(180deg);
        }
        
        .flip-card-front, .flip-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            border-radius: 15px;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 0 8px 25px var(--shadow-light);
            border: 2px solid transparent;
        }
        
        .flip-card-front {
            background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
            border: 2px solid var(--fdp-magenta);
        }
        
        .flip-card-back {
            background: linear-gradient(135deg, var(--fdp-magenta) 0%, #c91565 100%);
            color: white;
            transform: rotateY(180deg);
        }
        
        /* Symbol-Styling */
        .card-symbol {
            width: 80px;
            height: 80px;
            margin-bottom: 1rem;
            object-fit: cover;
            filter: drop-shadow(0 4px 8px var(--shadow-light));
            /* Entfernt weiße Ränder durch Clipping */
            clip-path: inset(8px 8px 8px 8px);
            border-radius: 10px;
            transition: var(--transition);
        }
        
        .card-symbol:hover {
            transform: scale(1.05);
            filter: drop-shadow(0 6px 12px var(--shadow-medium));
        }
        
        .card-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--fdp-dark);
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .card-subtitle {
            font-size: 0.9rem;
            opacity: 0.7;
            font-style: italic;
        }
        
        /* Rückseiten-Content */
        .position-content {
            text-align: left;
            width: 100%;
            overflow-y: auto;
            max-height: 200px;
        }
        
        .position-content h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--fdp-yellow);
            text-align: center;
            border-bottom: 2px solid var(--fdp-yellow);
            padding-bottom: 0.5rem;
        }
        
        .position-content p {
            font-size: 0.95rem;
            line-height: 1.5;
            margin-bottom: 0.8rem;
        }
        
        .position-content ul {
            margin-left: 1rem;
            margin-bottom: 0.8rem;
        }
        
        .position-content li {
            margin-bottom: 0.3rem;
        }
        
        /* Flip-Indikator */
        .flip-indicator {
            position: absolute;
            bottom: 10px;
            right: 10px;
            background: var(--fdp-yellow);
            color: var(--fdp-dark);
            border-radius: 50%;
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
            animation: pulse 2s infinite;
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        
        .flip-card:hover .flip-indicator {
            opacity: 0.5;
            transform: scale(1.05) rotate(180deg);
        }
        
        /* Footer */
        .footer {
            margin-top: 4rem;
            text-align: center;
            padding: 2rem;
            background: white;
            border-radius: 15px;
            box-shadow: 0 4px 15px var(--shadow-light);
            max-width: 1000px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .footer h3 {
            color: var(--fdp-magenta);
            margin-bottom: 1rem;
        }
        
        .legal-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 1rem;
        }
        
        .legal-links a {
            color: var(--fdp-blue);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .legal-links a:hover {
            color: var(--fdp-magenta);
            text-decoration: underline;
        }
        
        /* Animationen */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
                opacity: 1;
            }
            50% {
                transform: scale(1.1);
                opacity: 0.8;
            }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .logo-container {
                padding: 1rem 1.5rem;
                margin-bottom: 1.5rem;
            }
            
            .original-logo {
                max-width: 250px;
                padding: 1rem 1.5rem;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .positions-grid {
                grid-template-columns: 1fr;
                gap: 1.5rem;
                padding: 0.5rem;
            }
            
            .flip-card {
                height: 280px;
            }
            
            .flip-card-front, .flip-card-back {
                padding: 1.5rem;
            }
            
            .legal-links {
                flex-direction: column;
                gap: 1rem;
            }
        }
        
        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            
            .logo-container {
                padding: 0.8rem 1rem;
                margin-bottom: 1rem;
            }
            
            .original-logo {
                max-width: 200px;
                padding: 0.8rem 1rem;
            }
            
            .flip-card {
                height: 250px;
            }
            
            .card-symbol {
                width: 60px;
                height: 60px;
            }
            
            .card-title {
                font-size: 1.2rem;
            }
        }
        
        /* Accessibility */
        @media (prefers-reduced-motion: reduce) {
            * {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }
        
        .flip-card:focus {
            outline: 3px solid var(--fdp-yellow);
            outline-offset: 2px;
        }
        
        /* Print Styles */
        @media print {
            body {
                background: white;
            }
            
            .flip-card-back {
                position: relative;
                transform: none;
                display: block;
                margin-top: 1rem;
                color: black;
                background: #f0f0f0;
            }
        }
    </style>
</head>
<body>
    <!-- Skip Link für Accessibility -->
    <a href="#main-content" class="sr-only" style="position: absolute; left: -9999px; width: 1px; height: 1px; overflow: hidden;">Zum Hauptinhalt springen</a>
    
    <header class="header">
        <div class="logo-container">
            <img src="https://page.gensparksite.com/v1/base64_upload/c6d0f8a73ae2772dfcf472c28f7bcbf2" 
                 alt="FDP Märkischer Kreis Logo" 
                 class="original-logo"
                 loading="eager">
        </div>
        <h1>Unsere Positionen</h1>
        <p>Bewegen Sie die Maus über die Karten, um unsere Standpunkte zu den wichtigsten Themen für den Märkischen Kreis zu entdecken.</p>
    </header>
    
    <main id="main-content" class="positions-grid">
        
        <!-- Karte 1: Wirtschaft -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Wirtschaft anzeigen" data-theme="wirtschaft">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/6805f41a3b4ee092e25cd334262aada9" 
                         alt="Wirtschafts-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Wirtschaft</h2>
                    <p class="card-subtitle">Starke Unternehmen für den MK</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Wirtschaft</h3>
                        <p><strong>Der Märkische Kreis als starker Wirtschaftsstandort:</strong> Wir setzen auf die Kraft des freien Unternehmertums und schaffen optimale Bedingungen für Betriebe, Gründer und Arbeitsplätze in unserer Region.</p>
                        <ul>
                            <li><strong>Fast-Track für Genehmigungen:</strong> Betriebserweiterungen und Neuansiedlungen binnen 6 Monaten</li>
                            <li><strong>Digitale Verwaltung:</strong> Online-Anträge und papierlose Verfahren für Unternehmen</li>
                            <li><strong>Fachkräfte sichern:</strong> Ausbau dualer Ausbildung mit regionalen Partnern</li>
                            <li><strong>Bürokratie abbauen:</strong> "One-Stop-Shop" für Unternehmensgründungen</li>
                            <li><strong>Infrastruktur stärken:</strong> Schnelles Internet und modernste Verkehrsanbindung</li>
                        </ul>
                        <p>Unser Ziel: Der Märkische Kreis wird zur innovativsten und unternehmensfreundlichsten Region in NRW. Nur durch wirtschaftliche Stärke sichern wir Wohlstand und Arbeitsplätze für alle.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 2: Umwelt & Klima -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Umwelt und Klima anzeigen" data-theme="umwelt">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/06a900602293fbc3aff5ebfba326699d" 
                         alt="Umwelt-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Umwelt & Klima</h2>
                    <p class="card-subtitle">Nachhaltig in die Zukunft</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Umwelt & Klima</h3>
                        <p><strong>Innovation für den Klimaschutz:</strong> Wir setzen auf Technologie und marktwirtschaftliche Lösungen, um den Märkischen Kreis klimaneutral und gleichzeitig wirtschaftlich erfolgreich zu gestalten.</p>
                        <ul>
                            <li><strong>Technologieoffenheit:</strong> Wasserstoff, E-Mobilität und CO2-neutrale Industrie fördern</li>
                            <li><strong>Energieeffizienz:</strong> Moderne Wärmepumpen und Gebäudesanierung unterstützen</li>
                            <li><strong>Erneuerbare Energien:</strong> Ausbau von Wind- und Solarenergie mit Bürgerbeteiligung</li>
                            <li><strong>Kreislaufwirtschaft:</strong> Weniger Müll durch intelligente Recycling-Konzepte</li>
                            <li><strong>Naturschutz:</strong> Erhalt der schönen Landschaft im Sauerland und Märkischen Kreis</li>
                        </ul>
                        <p>Klimaschutz geht nur mit den Menschen, nicht gegen sie. Wir verbinden Ökologie und Ökonomie – für eine lebenswerte Zukunft im Märkischen Kreis.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 3: Bildung -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Bildung anzeigen" data-theme="bildung">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/ab07f8f347c8f68cbf00d37670d1328b" 
                         alt="Bildungs-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Bildung</h2>
                    <p class="card-subtitle">Beste Chancen für alle</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Bildung</h3>
                        <p><strong>Beste Bildung für beste Chancen:</strong> Jedes Kind im Märkischen Kreis soll die Chance haben, das Beste aus seinen Talenten zu machen – unabhängig von Herkunft oder Geldbeutel der Eltern.</p>
                        <ul>
                            <li><strong>Digitale Schulen:</strong> Schnelles WLAN und moderne Ausstattung an allen Schulen</li>
                            <li><strong>Duale Ausbildung stärken:</strong> Enge Kooperation zwischen Berufskollegs und regionalen Unternehmen</li>
                            <li><strong>Lehrer unterstützen:</strong> Weniger Bürokratie, mehr Zeit für Schüler</li>
                            <li><strong>MINT-Förderung:</strong> Mathematik, Informatik, Naturwissenschaft und Technik gezielt stärken</li>
                            <li><strong>Lebenslanges Lernen:</strong> Weiterbildungsmöglichkeiten für alle Altersgruppen</li>
                        </ul>
                        <p>Bildung ist der Rohstoff der Zukunft. Der Märkische Kreis braucht gut ausgebildete Fachkräfte – und jeder Mensch hat das Recht auf bestmögliche Bildung.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 4: Finanzen -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Finanzen anzeigen" data-theme="finanzen">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/63feececdc2dad427c4d2ef9d0baab1e" 
                         alt="Finanz-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Finanzen</h2>
                    <p class="card-subtitle">Solide Haushaltspolitik</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Finanzen</h3>
                        <p><strong>Solide Finanzen für eine starke Zukunft:</strong> Der Märkische Kreis muss wirtschaftlich verantwortlich handeln – sparsam bei laufenden Ausgaben, mutig bei zukunftsweisenden Investitionen.</p>
                        <ul>
                            <li><strong>Ausgaben priorisieren:</strong> Jeder Euro muss einen Nutzen für die Bürger bringen</li>
                            <li><strong>Investitionen in die Zukunft:</strong> Straßen, Schulen, Digitalisierung und Wirtschaftsförderung</li>
                            <li><strong>Transparenz schaffen:</strong> Verständliche Haushaltsdarstellung für alle Bürger</li>
                            <li><strong>Verschuldung begrenzen:</strong> Heute nicht auf Kosten künftiger Generationen leben</li>
                            <li><strong>Gebühren fair gestalten:</strong> Kostenwahrheit bei kommunalen Dienstleistungen</li>
                        </ul>
                        <p>Schwarze Zahlen sind kein Selbstzweck, sondern die Basis für Gestaltungsspielräume. Nur wer solide wirtschaftet, kann auch in Krisen handlungsfähig bleiben.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 5: Digitalisierung -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Digitalisierung anzeigen" data-theme="digitalisierung">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/278d35cc81f9dd34c568e9b0b37c63e4" 
                         alt="Digital-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Digitalisierung</h2>
                    <p class="card-subtitle">Innovation für den MK</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Digitalisierung</h3>
                        <p><strong>Der Märkische Kreis wird digital:</strong> Glasfaser bis in jeden Ortsteil, digitale Verwaltung und innovative Unternehmen – wir bringen die Region ins 21. Jahrhundert.</p>
                        <ul>
                            <li><strong>Flächendeckender Glasfaserausbau:</strong> Gigabit-Internet auch im ländlichen Raum</li>
                            <li><strong>Digitales Rathaus:</strong> Alle Behördengänge online möglich, 24/7 verfügbar</li>
                            <li><strong>5G-Mobilfunk:</strong> Lückenlose Netzabdeckung für Wirtschaft und Bürger</li>
                            <li><strong>Start-up-Förderung:</strong> Digitale Gründerzentren und Tech-Inkubatoren</li>
                            <li><strong>Cybersicherheit:</strong> Schutz der digitalen Infrastruktur und Bürgerdaten</li>
                        </ul>
                        <p>Digitalisierung ist keine Option, sondern Pflicht. Der Märkische Kreis darf nicht den Anschluss verlieren – wir gestalten die digitale Zukunft aktiv mit.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 6: Integration -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Integration anzeigen" data-theme="integration">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/13ab719b71238ac92cfa151d20935e62" 
                         alt="Integrations-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Integration</h2>
                    <p class="card-subtitle">Zusammenhalt stärken</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Integration</h3>
                        <p><strong>Zusammenleben durch Zusammenarbeit:</strong> Integration gelingt durch Chancen auf Teilhabe, klare Regeln und die Bereitschaft aller Seiten, unsere freiheitlichen Werte zu leben.</p>
                        <ul>
                            <li><strong>Sprache als Schlüssel:</strong> Intensive Deutschkurse von Anfang an für alle Zuwanderer</li>
                            <li><strong>Arbeitsmarktintegration:</strong> Schnelle Anerkennung von Qualifikationen und Umschulungen</li>
                            <li><strong>Bildungschancen:</strong> Förderung für Kinder und Jugendliche mit Migrationshintergrund</li>
                            <li><strong>Ehrenamt stärken:</strong> Unterstützung für Vereine und Organisationen in der Integrationsarbeit</li>
                            <li><strong>Werte vermitteln:</strong> Respekt für Demokratie, Gleichberechtigung und Rechtsstaatlichkeit</li>
                        </ul>
                        <p>Integration ist eine Bringschuld aller: Die Gesellschaft muss Chancen bieten, Zuwanderer müssen sie nutzen. Gemeinsam schaffen wir ein friedliches Miteinander im Märkischen Kreis.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 7: Verkehr & Mobilität -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Verkehr und Mobilität anzeigen" data-theme="verkehr">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/23bb8e4d39412bb8571457a27d026703" 
                         alt="Verkehrs-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Verkehr & Mobilität</h2>
                    <p class="card-subtitle">Moderne Infrastruktur</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Verkehr & Mobilität</h3>
                        <p><strong>Moderne Mobilität für alle:</strong> Egal ob Auto, Bus, Bahn oder Fahrrad – im Märkischen Kreis soll jeder schnell, sicher und bezahlbar von A nach B kommen.</p>
                        <ul>
                            <li><strong>Straßen sanieren:</strong> Systematische Erneuerung der Kreisstraßen und Brücken</li>
                            <li><strong>ÖPNV stärken:</strong> Bessere Taktung, moderne Busse und digitale Fahrgastinformation</li>
                            <li><strong>Radverkehr fördern:</strong> Sichere Radwege und E-Bike-Ladestationen</li>
                            <li><strong>Park & Ride:</strong> Pendlerparkplätze an Bahnhöfen und Bushaltestellen</li>
                            <li><strong>Elektromobilität:</strong> Flächendeckendes Netz von Ladesäulen</li>
                        </ul>
                        <p>Mobilität bedeutet Freiheit. Wir setzen auf Technologieoffenheit und Wahlfreiheit – nicht auf Verbote und Bevormundung. Der Märkische Kreis wird zur Modellregion für moderne Mobilität.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 8: Sicherheit & Sauberkeit -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Sicherheit und Sauberkeit anzeigen" data-theme="sicherheit">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/1df5c7b3e22f3e7b089d05dc4870499d" 
                         alt="Sicherheits-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Sicherheit & Sauberkeit</h2>
                    <p class="card-subtitle">Schutz und Ordnung</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Sicherheit & Sauberkeit</h3>
                        <p><strong>Sicherheit und Ordnung sind Bürgerpflicht:</strong> Jeder soll sich im Märkischen Kreis sicher fühlen können – in Parks, auf Straßen, an Bahnhöfen und in der eigenen Nachbarschaft.</p>
                        <ul>
                            <li><strong>Ordnungsamt stärken:</strong> Mehr Personal für Kontrollen und Bürgernähe vor Ort</li>
                            <li><strong>Videoüberwachung:</strong> An kritischen Punkten für mehr Sicherheit und Aufklärung</li>
                            <li><strong>Sauberkeit durchsetzen:</strong> Konsequente Ahndung von Müll, Vandalismus und Graffiti</li>
                            <li><strong>Beleuchtung verbessern:</strong> Helle, sichere Wege und Plätze</li>
                            <li><strong>Bürgerwehren unterstützen:</strong> Ehrenamtliche Sicherheitspartnerschaften fördern</li>
                        </ul>
                        <p>Sicherheit ist ein Grundrecht. Wo Gesetze nicht eingehalten werden, muss der Staat konsequent handeln – zum Schutz aller rechtstreuen Bürger.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 9: Kultur & Sport -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Kultur und Sport anzeigen" data-theme="kultur">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/6a3d5f48f2d3199fe56f41571c5dbc1b" 
                         alt="Kultur-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Kultur & Sport</h2>
                    <p class="card-subtitle">Vielfalt fördern</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Kultur & Sport</h3>
                        <p><strong>Lebensqualität durch Vielfalt:</strong> Kultur und Sport machen das Leben im Märkischen Kreis lebenswert – sie fördern Gemeinschaft, Gesundheit und Kreativität.</p>
                        <ul>
                            <li><strong>Vereine unterstützen:</strong> Weniger Bürokratie, mehr finanzielle Förderung für ehrenamtliche Arbeit</li>
                            <li><strong>Sportanlagen modernisieren:</strong> Investitionen in Schwimmbäder, Sporthallen und Fußballplätze</li>
                            <li><strong>Kulturförderung:</strong> Theater, Museen und Musikschulen als Bildungsorte stärken</li>
                            <li><strong>Jugendarbeit:</strong> Freizeitzentren und Jugendtreffs in allen Kommunen</li>
                            <li><strong>Barrierefreiheit:</strong> Kultur und Sport für Menschen mit Handicap zugänglich machen</li>
                        </ul>
                        <p>Kultur und Sport sind mehr als Freizeitbeschäftigung – sie bilden das soziale Rückgrat unserer Gesellschaft. Wir investieren in die Lebensqualität aller Generationen.</p>
                    </div>
                </div>
            </div>
        </article>

        <!-- Karte 10: Wohnen & Bauen -->
        <article class="flip-card" role="button" tabindex="0" aria-label="Position zu Wohnen und Bauen anzeigen" data-theme="wohnen">
            <div class="flip-card-inner">
                <div class="flip-card-front">
                    <img src="https://page.gensparksite.com/v1/base64_upload/776fbd84fc3a95fd2dc95bce589a93b7" 
                         alt="Wohn-Symbol" class="card-symbol" loading="lazy">
                    <h2 class="card-title">Wohnen & Bauen</h2>
                    <p class="card-subtitle">Bezahlbar leben</p>
                    <div class="flip-indicator">↻</div>
                </div>
                <div class="flip-card-back">
                    <div class="position-content">
                        <h3>FDP MK Position: Wohnen & Bauen</h3>
                        <p><strong>Bezahlbar wohnen, schneller bauen:</strong> Junge Familien und Senioren brauchen passenden Wohnraum im Märkischen Kreis – ohne jahrelange Wartezeiten und Bürokratie-Marathon.</p>
                        <ul>
                            <li><strong>Bau-Bürokratie abbauen:</strong> Digitale Anträge, kürzere Genehmigungsverfahren</li>
                            <li><strong>Bauland schaffen:</strong> Innenentwicklung vor Flächenverbrauch, intelligente Nachverdichtung</li>
                            <li><strong>Eigentumsförderung:</strong> Mehr Menschen sollen sich Wohneigentum leisten können</li>
                            <li><strong>Altersgerechtes Wohnen:</strong> Barrierefreie Wohnungen und betreutes Wohnen ausbauen</li>
                            <li><strong>Energie-Standards:</strong> Moderne, aber bezahlbare Energieeffizienz beim Neubau</li>
                        </ul>
                        <p>Wohnen ist ein Grundbedürfnis. Durch weniger Vorschriften und mehr Angebot schaffen wir bezahlbaren Wohnraum für alle – ohne die Umwelt zu belasten.</p>
                    </div>
                </div>
            </div>
        </article>

    </main>
    
    <footer class="footer">
        <div style="background: #ffffff; padding: 1rem 1.5rem; border-radius: 15px; border: 2px solid var(--fdp-magenta); display: inline-block; box-shadow: 0 4px 15px var(--shadow-light);">
            <img src="https://page.gensparksite.com/v1/base64_upload/c6d0f8a73ae2772dfcf472c28f7bcbf2" 
                 alt="FDP Märkischer Kreis Logo" 
                 style="max-width: 200px; width: 100%; height: auto;"
                 loading="lazy">
        </div>
        <p><strong>Für Freiheit, Fortschritt und faire Chancen im Märkischen Kreis.</strong></p>
        <p style="font-style: italic; margin-top: 0.5rem;">Liberal. Bürgerlich. Fortschrittlich. – Ihre Stimme für moderne Politik vor Ort.</p>
        
        <div class="legal-links">
            <a href="#impressum" onclick="openModal('impressum')">Impressum</a>
            <a href="#datenschutz" onclick="openModal('datenschutz')">Datenschutz</a>
            <a href="#nutzungsbedingungen" onclick="openModal('nutzungsbedingungen')">Nutzungsbedingungen</a>
            <a href="https://www.fdp-nrw.de" target="_blank" rel="noopener noreferrer">FDP NRW</a>
        </div>
        
        <p style="margin-top: 1rem; font-size: 0.9rem; opacity: 0.7;">
            © 2025 FDP Märkischer Kreis. Diese Seite verwendet keine Cookies und sammelt keine persönlichen Daten.
        </p>
    </footer>

    <!-- Modal für rechtliche Inhalte -->
    <div id="legal-modal" style="display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); z-index: 1000; overflow-y: auto;">
        <div style="background: white; margin: 50px auto; padding: 2rem; border-radius: 15px; max-width: 800px; position: relative;">
            <button onclick="closeModal()" style="position: absolute; top: 10px; right: 15px; background: none; border: none; font-size: 1.5rem; cursor: pointer;">×</button>
            <div id="modal-content"></div>
        </div>
    </div>

    <script>
        // Flip-Karten Funktionalität
        document.addEventListener('DOMContentLoaded', function() {
            const flipCards = document.querySelectorAll('.flip-card');
            
            flipCards.forEach(card => {
                // Hover-Event für Desktop (automatisches Umdrehen bei Maus drauf)
                // CSS :hover übernimmt das automatisch
                
                // Click Event für zusätzliche Interaktion (Toggle-Funktion)
                card.addEventListener('click', function(e) {
                    e.preventDefault();
                    this.classList.toggle('flipped');
                });
                
                // Keyboard Support
                card.addEventListener('keydown', function(e) {
                    if (e.key === 'Enter' || e.key === ' ') {
                        e.preventDefault();
                        this.classList.toggle('flipped');
                    }
                });
                
                // Touch Support für mobile Geräte (da kein Hover auf Touch-Geräten)
                let touchStartTime = 0;
                card.addEventListener('touchstart', function() {
                    touchStartTime = Date.now();
                });
                
                card.addEventListener('touchend', function(e) {
                    const touchDuration = Date.now() - touchStartTime;
                    if (touchDuration < 500) { // Kurzer Tap
                        e.preventDefault();
                        this.classList.toggle('flipped');
                    }
                });
                
                // Mouse Leave Event - Karte dreht sich zurück wenn Maus weg geht
                card.addEventListener('mouseleave', function() {
                    // Nur zurückdrehen wenn nicht durch Klick "fixiert"
                    if (!this.classList.contains('flipped')) {
                        // Die CSS :hover Regel sorgt automatisch für das Zurückdrehen
                    }
                });
            });
            
            // Staggered Animation beim Laden
            flipCards.forEach((card, index) => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(50px)';
                
                setTimeout(() => {
                    card.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }, index * 150);
            });
        });
        
        // Modal-Funktionen für rechtliche Inhalte
        function openModal(type) {
            const modal = document.getElementById('legal-modal');
            const content = document.getElementById('modal-content');
            
            let modalContent = '';
            
            if (type === 'impressum') {
                modalContent = `
                    <h2>Impressum</h2>
                    <h3>Angaben gemäß § 5 TMG</h3>
                    <p><strong>FDP Märkischer Kreis</strong><br>
                    [Hier Ihre Adresse einfügen]<br>
                    [PLZ] [Ort]</p>
                    
                    <h3>Vertreten durch:</h3>
                    <p>[Name des Vorsitzenden]<br>
                    Telefon: [Telefonnummer]<br>
                    E-Mail: [E-Mail-Adresse]</p>
                    
                    <h3>Verantwortlich für den Inhalt nach § 55 Abs. 2 RStV:</h3>
                    <p>[Name des Verantwortlichen]<br>
                    [Adresse]</p>
                `;
            } else if (type === 'datenschutz') {
                modalContent = `
                    <h2>Datenschutzerklärung</h2>
                    <h3>1. Grundsätzliches</h3>
                    <p>Diese Website sammelt keine persönlichen Daten und verwendet keine Cookies. Ihre Privatsphäre ist uns wichtig.</p>
                    
                    <h3>2. Server-Log-Dateien</h3>
                    <p>Bei jedem Aufruf unserer Internetseite erfasst unser System automatisiert Daten und Informationen vom Computersystem des aufrufenden Rechners.</p>
                    
                    <h3>3. Ihre Rechte</h3>
                    <p>Sie haben das Recht auf Auskunft, Berichtigung, Löschung und Einschränkung der Verarbeitung Ihrer personenbezogenen Daten.</p>
                    
                    <h3>4. Kontakt</h3>
                    <p>Bei Fragen zum Datenschutz wenden Sie sich an: [Datenschutz-E-Mail]</p>
                `;
            } else if (type === 'nutzungsbedingungen') {
                modalContent = `
                    <h2>Nutzungsbedingungen</h2>
                    <h3>1. Geltungsbereich</h3>
                    <p>Diese Nutzungsbedingungen gelten für die Nutzung der Website der FDP Märkischer Kreis.</p>
                    
                    <h3>2. Urheberrecht</h3>
                    <p>Die Inhalte und Werke auf diesen Seiten unterliegen dem deutschen Urheberrecht.</p>
                    
                    <h3>3. Haftungsausschluss</h3>
                    <p>Die Inhalte unserer Seiten wurden mit größter Sorgfalt erstellt. Für die Richtigkeit, Vollständigkeit und Aktualität der Inhalte können wir jedoch keine Gewähr übernehmen.</p>
                    
                    <h3>4. Links zu externen Websites</h3>
                    <p>Unsere Website enthält Links zu externen Websites. Auf deren Inhalte haben wir keinen Einfluss.</p>
                `;
            }
            
            content.innerHTML = modalContent;
            modal.style.display = 'block';
            document.body.style.overflow = 'hidden';
        }
        
        function closeModal() {
            const modal = document.getElementById('legal-modal');
            modal.style.display = 'none';
            document.body.style.overflow = 'auto';
        }
        
        // Modal schließen bei Klick außerhalb
        document.getElementById('legal-modal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });
        
        // ESC-Taste zum Schließen
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                closeModal();
            }
        });
        
        // Performance Optimierung
        if ('loading' in HTMLImageElement.prototype) {
            // Native lazy loading unterstützt
            console.log('Native lazy loading wird verwendet');
        } else {
            // Fallback für ältere Browser
            const images = document.querySelectorAll('img[loading="lazy"]');
            images.forEach(img => {
                img.src = img.src;
            });
        }
    </script>
</body>
</html>
