<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Gopikrishnan S · GitHub Profile</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
    <style>
        /* ----- Reset & Base ----- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;
            display: flex;
            justify-content: center;
            padding: 40px 20px;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            color: #c9d1d9;
            line-height: 1.6;
        }

        .readme {
            max-width: 880px;
            width: 100%;
            background: #161b22;
            border-radius: 24px;
            padding: 40px 36px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7);
            border: 1px solid #30363d;
            transition: all 0.3s ease;
        }

        /* ----- Scrollbar ----- */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0d1117;
        }
        ::-webkit-scrollbar-thumb {
            background: #30363d;
            border-radius: 10px;
        }

        /* ----- Typography ----- */
        h1,
        h2,
        h3 {
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        a {
            color: #58a6ff;
            text-decoration: none;
            transition: color 0.2s;
        }
        a:hover {
            color: #79c0ff;
            text-decoration: underline;
        }

        .text-muted {
            color: #8b949e;
        }
        .text-accent {
            color: #58a6ff;
        }
        .text-green {
            color: #3fb950;
        }
        .text-gold {
            color: #f0883e;
        }
        .text-purple {
            color: #d2a8ff;
        }

        /* ----- Header / Avatar ----- */
        .header {
            display: flex;
            align-items: center;
            gap: 24px;
            flex-wrap: wrap;
            margin-bottom: 28px;
        }

        .avatar-wrapper {
            position: relative;
            flex-shrink: 0;
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #1f6feb, #58a6ff);
            padding: 3px;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: avatarPulse 3s ease-in-out infinite;
        }

        .avatar img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #0d1117;
            background: #161b22;
        }

        @keyframes avatarPulse {
            0%,
            100% {
                transform: scale(1);
                box-shadow: 0 0 0 0 rgba(88, 166, 255, 0.3);
            }
            50% {
                transform: scale(1.02);
                box-shadow: 0 0 30px 8px rgba(88, 166, 255, 0.15);
            }
        }

        .header-info h1 {
            font-size: 2.4rem;
            color: #f0f6fc;
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
        }

        .header-info h1 .badge-verified {
            background: #1f6feb;
            color: #fff;
            font-size: 0.7rem;
            font-weight: 600;
            padding: 2px 10px;
            border-radius: 20px;
            display: inline-flex;
            align-items: center;
            gap: 4px;
            letter-spacing: 0.3px;
        }

        .header-info .subtitle {
            font-size: 1.15rem;
            color: #8b949e;
            margin-top: 4px;
        }

        .header-info .typing-wrap {
            font-size: 1.1rem;
            color: #f0f6fc;
            margin-top: 6px;
            display: flex;
            align-items: center;
            gap: 6px;
            flex-wrap: wrap;
        }

        .typing-wrap .static {
            color: #8b949e;
        }

        .typing-wrap .dynamic {
            color: #58a6ff;
            font-weight: 600;
            border-right: 2px solid #58a6ff;
            padding-right: 4px;
            animation: blink 0.9s step-end infinite;
        }

        @keyframes blink {
            50% {
                border-color: transparent;
            }
        }

        /* ----- Social Icons ----- */
        .social-bar {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
            margin: 16px 0 24px 0;
            padding: 12px 0;
            border-top: 1px solid #21262d;
            border-bottom: 1px solid #21262d;
        }

        .social-bar a {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #8b949e;
            font-size: 0.95rem;
            transition: color 0.2s, transform 0.2s;
        }

        .social-bar a:hover {
            color: #f0f6fc;
            transform: translateY(-2px);
            text-decoration: none;
        }

        .social-bar a i {
            font-size: 1.3rem;
            width: 24px;
            text-align: center;
        }

        /* ----- Badge Grid ----- */
        .badge-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 12px 16px;
            margin: 20px 0 28px 0;
            padding: 16px 18px;
            background: #0d1117;
            border-radius: 16px;
            border: 1px solid #21262d;
        }

        .badge-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            background: #21262d;
            padding: 6px 14px 6px 10px;
            border-radius: 40px;
            transition: background 0.2s, transform 0.2s;
        }

        .badge-item:hover {
            background: #30363d;
            transform: scale(1.03);
        }

        .badge-item i {
            font-size: 1rem;
            color: #58a6ff;
        }

        .badge-item .label {
            color: #c9d1d9;
        }

        .badge-item .value {
            font-weight: 600;
            color: #f0f6fc;
        }

        /* ----- Section Titles ----- */
        .section-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: #f0f6fc;
            margin: 32px 0 16px 0;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .section-title i {
            color: #58a6ff;
            font-size: 1.3rem;
        }

        .section-title::after {
            content: '';
            flex: 1;
            height: 1px;
            background: linear-gradient(90deg, #30363d, transparent);
        }

        /* ----- Skills (animated pills) ----- */
        .skills-wrap {
            display: flex;
            flex-wrap: wrap;
            gap: 10px 14px;
            margin: 12px 0 8px 0;
        }

        .skill-pill {
            background: #21262d;
            padding: 6px 18px;
            border-radius: 40px;
            font-size: 0.9rem;
            font-weight: 500;
            border: 1px solid #30363d;
            transition: all 0.3s ease;
            animation: skillFloat 4s ease-in-out infinite;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .skill-pill i {
            font-size: 0.9rem;
            color: #58a6ff;
        }

        .skill-pill:hover {
            transform: translateY(-4px) scale(1.04);
            border-color: #58a6ff;
            box-shadow: 0 8px 20px rgba(88, 166, 255, 0.15);
            background: #1c2333;
        }

        .skill-pill:nth-child(1) {
            animation-delay: 0s;
        }
        .skill-pill:nth-child(2) {
            animation-delay: 0.3s;
        }
        .skill-pill:nth-child(3) {
            animation-delay: 0.6s;
        }
        .skill-pill:nth-child(4) {
            animation-delay: 0.9s;
        }
        .skill-pill:nth-child(5) {
            animation-delay: 1.2s;
        }
        .skill-pill:nth-child(6) {
            animation-delay: 1.5s;
        }
        .skill-pill:nth-child(7) {
            animation-delay: 1.8s;
        }
        .skill-pill:nth-child(8) {
            animation-delay: 2.1s;
        }
        .skill-pill:nth-child(9) {
            animation-delay: 2.4s;
        }
        .skill-pill:nth-child(10) {
            animation-delay: 2.7s;
        }

        @keyframes skillFloat {
            0%,
            100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-3px);
            }
        }

        /* ----- Cards (projects, certs) ----- */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 18px;
            margin: 16px 0 8px 0;
        }

        .card {
            background: #0d1117;
            border: 1px solid #21262d;
            border-radius: 16px;
            padding: 18px 20px 20px 20px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #58a6ff, #1f6feb);
            opacity: 0;
            transition: opacity 0.3s;
        }

        .card:hover {
            border-color: #30363d;
            transform: translateY(-4px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.5);
        }

        .card:hover::after {
            opacity: 1;
        }

        .card .card-icon {
            font-size: 1.6rem;
            color: #58a6ff;
            margin-bottom: 6px;
        }

        .card h3 {
            font-size: 1.1rem;
            color: #f0f6fc;
            margin-bottom: 4px;
        }

        .card p {
            font-size: 0.9rem;
            color: #8b949e;
            line-height: 1.5;
        }

        .card .meta {
            font-size: 0.8rem;
            color: #8b949e;
            margin-top: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
        }

        .card .meta i {
            color: #58a6ff;
        }

        .card .tag {
            display: inline-block;
            background: #21262d;
            padding: 2px 10px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 500;
            color: #c9d1d9;
            margin-top: 6px;
        }

        /* ----- Stats Row (GitHub style) ----- */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            gap: 16px 30px;
            background: #0d1117;
            border-radius: 16px;
            padding: 18px 22px;
            margin: 20px 0 16px 0;
            border: 1px solid #21262d;
        }

        .stat-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .stat-item i {
            font-size: 1.3rem;
            color: #58a6ff;
            width: 28px;
            text-align: center;
        }

        .stat-item .num {
            font-weight: 700;
            font-size: 1.2rem;
            color: #f0f6fc;
        }

        .stat-item .lbl {
            color: #8b949e;
            font-size: 0.9rem;
        }

        /* ----- Contribution heatmap mock ----- */
        .heatmap {
            display: grid;
            grid-template-columns: repeat(52, 1fr);
            gap: 3px;
            margin: 16px 0 8px 0;
            background: #0d1117;
            border-radius: 12px;
            padding: 14px 12px;
            border: 1px solid #21262d;
        }

        .heatmap .day {
            aspect-ratio: 1;
            border-radius: 3px;
            background: #161b22;
            transition: background 0.3s;
            animation: heatPulse 2s ease-in-out infinite alternate;
        }

        .heatmap .day.l1 {
            background: #0e4429;
        }
        .heatmap .day.l2 {
            background: #006d32;
        }
        .heatmap .day.l3 {
            background: #26a641;
        }
        .heatmap .day.l4 {
            background: #39d353;
        }
        .heatmap .day.l5 {
            background: #56d364;
        }

        .heatmap .day:nth-child(7n+1) {
            background: #1f6feb;
        }
        .heatmap .day:nth-child(13n+4) {
            background: #0e4429;
        }
        .heatmap .day:nth-child(23n+7) {
            background: #26a641;
        }
        .heatmap .day:nth-child(31n+2) {
            background: #39d353;
        }
        .heatmap .day:nth-child(41n+9) {
            background: #006d32;
        }
        .heatmap .day:nth-child(47n+5) {
            background: #1f6feb;
        }

        @keyframes heatPulse {
            0% {
                opacity: 0.8;
            }
            100% {
                opacity: 1;
            }
        }

        .heatmap-legend {
            display: flex;
            justify-content: flex-end;
            align-items: center;
            gap: 4px;
            font-size: 0.7rem;
            color: #8b949e;
            margin-top: 4px;
        }

        .heatmap-legend .swatch {
            width: 14px;
            height: 14px;
            border-radius: 3px;
            background: #161b22;
        }
        .heatmap-legend .swatch.l1 {
            background: #0e4429;
        }
        .heatmap-legend .swatch.l2 {
            background: #006d32;
        }
        .heatmap-legend .swatch.l3 {
            background: #26a641;
        }
        .heatmap-legend .swatch.l4 {
            background: #39d353;
        }
        .heatmap-legend .swatch.l5 {
            background: #56d364;
        }

        /* ----- Footer ----- */
        .footer-note {
            text-align: center;
            font-size: 0.85rem;
            color: #8b949e;
            margin-top: 36px;
            padding-top: 20px;
            border-top: 1px solid #21262d;
        }

        .footer-note i {
            color: #f0883e;
            animation: heartBeat 1.6s ease-in-out infinite;
        }

        @keyframes heartBeat {
            0%,
            100% {
                transform: scale(1);
            }
            15% {
                transform: scale(1.2);
            }
            30% {
                transform: scale(1);
            }
            45% {
                transform: scale(1.15);
            }
            60% {
                transform: scale(1);
            }
        }

        /* ----- Responsive ----- */
        @media (max-width: 640px) {
            .readme {
                padding: 24px 16px;
            }
            .header {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }
            .header-info h1 {
                font-size: 1.8rem;
                justify-content: center;
            }
            .typing-wrap {
                justify-content: center;
            }
            .social-bar {
                justify-content: center;
            }
            .badge-grid {
                justify-content: center;
            }
            .stats-row {
                justify-content: center;
            }
            .heatmap {
                grid-template-columns: repeat(26, 1fr);
                padding: 10px 8px;
            }
            .card-grid {
                grid-template-columns: 1fr;
            }
            .section-title {
                font-size: 1.3rem;
            }
        }

        @media (max-width: 440px) {
            .heatmap {
                grid-template-columns: repeat(18, 1fr);
            }
            .badge-item {
                font-size: 0.75rem;
                padding: 4px 10px 4px 8px;
            }
        }

        /* extra glow */
        .glow-text {
            text-shadow: 0 0 30px rgba(88, 166, 255, 0.08);
        }
    </style>
</head>
<body>

    <div class="readme">

        <!-- ===== HEADER ===== -->
        <div class="header">
            <div class="avatar-wrapper">
                <div class="avatar">
                    <img src="https://media.licdn.com/dms/image/v2/D5635AQGJRQNA7uPRmA/profile-framedphoto-shrink_200_200/B56Zz.rbJXGgAY-/0/1773799322971?e=1788112800&v=beta&t=fM3RSLR11gyPJksF8Yo2uupBNVZ5qi3Eqb8L_foZdag" alt="Gopikrishnan S" />
                </div>
            </div>
            <div class="header-info">
                <h1>
                    Gopikrishnan S
                    <span class="badge-verified">
                        <i class="fas fa-check-circle"></i> Verified
                    </span>
                </h1>
                <div class="subtitle">
                    <i class="fas fa-graduation-cap" style="color:#58a6ff;"></i>
                    Cybersecurity Student · CTF Player · TryHackMe Top 3%
                </div>
                <div class="typing-wrap">
                    <span class="static">🔐</span>
                    <span class="dynamic" id="typingText"></span>
                </div>
            </div>
        </div>

        <!-- ===== SOCIAL BAR ===== -->
        <div class="social-bar">
            <a href="https://linkedin.com/in/gopikrishnans07" target="_blank">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
            <a href="https://github.com/gopikrishnans07" target="_blank">
                <i class="fab fa-github"></i> GitHub
            </a>
            <a href="https://tryhackme.com/p/gopikrishnans07" target="_blank">
                <i class="fas fa-terminal"></i> TryHackMe
            </a>
            <a href="https://hackviser.com/verify?id=HV-CORE-K6JX40T5" target="_blank">
                <i class="fas fa-certificate"></i> Hackviser
            </a>
            <a href="mailto:gopikrishnans@example.com">
                <i class="fas fa-envelope"></i> Email
            </a>
        </div>

        <!-- ===== BADGE GRID ===== -->
        <div class="badge-grid">
            <div class="badge-item">
                <i class="fas fa-user-graduate"></i>
                <span class="label">Education</span>
                <span class="value">BE Cyber Security</span>
            </div>
            <div class="badge-item">
                <i class="fas fa-map-pin"></i>
                <span class="label">Location</span>
                <span class="value">Greater Coimbatore</span>
            </div>
            <div class="badge-item">
                <i class="fas fa-users"></i>
                <span class="label">Followers</span>
                <span class="value">3.2K+</span>
            </div>
            <div class="badge-item">
                <i class="fas fa-trophy"></i>
                <span class="label">THM</span>
                <span class="value">Top 3%</span>
            </div>
            <div class="badge-item">
                <i class="fas fa-certificate"></i>
                <span class="label">Certs</span>
                <span class="value">6</span>
            </div>
            <div class="badge-item">
                <i class="fas fa-code"></i>
                <span class="label">Projects</span>
                <span class="value">4+</span>
            </div>
        </div>

        <!-- ===== ABOUT / INTRO ===== -->
        <div style="margin: 8px 0 4px 0; font-size: 1rem; color: #c9d1d9; line-height: 1.7;">
            <p>
                <i class="fas fa-quote-left" style="color:#58a6ff; opacity:0.6; margin-right:6px;"></i>
                Cybersecurity isn't just about learning tools — it's about understanding how systems work,
                how vulnerabilities happen, and how to think like both a defender and an attacker.
                <i class="fas fa-quote-right" style="color:#58a6ff; opacity:0.6; margin-left:6px;"></i>
            </p>
            <p style="margin-top: 8px; color: #8b949e; font-size: 0.95rem;">
                🎯 Every lab, CTF, and practical exercise adds another piece to the puzzle.
                <span style="color:#58a6ff;">#LearningInPublic</span>
                <span style="color:#f0883e;">#CyberSecurityJourney</span>
            </p>
        </div>

        <!-- ===== SKILLS ===== -->
        <div class="section-title">
            <i class="fas fa-cogs"></i> Technical Arsenal
        </div>
        <div class="skills-wrap">
            <span class="skill-pill"><i class="fas fa-shield-alt"></i> Penetration Testing</span>
            <span class="skill-pill"><i class="fas fa-database"></i> SQL Injection</span>
            <span class="skill-pill"><i class="fas fa-code"></i> Java</span>
            <span class="skill-pill"><i class="fab fa-python"></i> Python</span>
            <span class="skill-pill"><i class="fas fa-terminal"></i> Linux / Bash</span>
            <span class="skill-pill"><i class="fas fa-lock"></i> Cryptography</span>
            <span class="skill-pill"><i class="fas fa-cloud"></i> Cloud Security</span>
            <span class="skill-pill"><i class="fas fa-bug"></i> Vulnerability Analysis</span>
            <span class="skill-pill"><i class="fas fa-network-wired"></i> Network Security</span>
            <span class="skill-pill"><i class="fas fa-robot"></i> AI / ML Security</span>
            <span class="skill-pill"><i class="fas fa-user-secret"></i> Red Teaming</span>
            <span class="skill-pill"><i class="fas fa-search"></i> OSINT</span>
        </div>

        <!-- ===== CERTIFICATIONS ===== -->
        <div class="section-title">
            <i class="fas fa-certificate"></i> Licenses &amp; Certifications
        </div>
        <div class="card-grid">
            <div class="card">
                <div class="card-icon"><i class="fas fa-shield-halved"></i></div>
                <h3>Certified Cybersecurity Foundations</h3>
                <p>Hackviser · Issued Aug 2026</p>
                <div class="meta">
                    <i class="fas fa-id-card"></i> HV-CORE-K6JX40T5
                    <span class="tag"><i class="fas fa-check-circle" style="color:#3fb950;"></i> Verified</span>
                </div>
            </div>
            <div class="card">
                <div class="card-icon"><i class="fab fa-java"></i></div>
                <h3>Java (Basic)</h3>
                <p>HackerRank · Issued Jan 2026</p>
                <div class="meta">
                    <i class="fas fa-id-card"></i> 43f3fa61ebb4
                    <span class="tag"><i class="fas fa-check-circle" style="color:#3fb950;"></i> Verified</span>
                </div>
            </div>
            <div class="card">
                <div class="card-icon"><i class="fas fa-bolt"></i></div>
                <h3>Hacker Holidays 2026</h3>
                <p>TryHackMe · 14‑day challenge</p>
                <div class="meta">
                    <i class="fas fa-calendar-check"></i> Completed Aug 2026
                    <span class="tag"><i class="fas fa-trophy" style="color:#f0883e;"></i> Certificate</span>
                </div>
            </div>
            <div class="card">
                <div class="card-icon"><i class="fas fa-skull"></i></div>
                <h3>Penetesting Lab</h3>
                <p>HebeSec · 4 challenges solved</p>
                <div class="meta">
                    <i class="fas fa-flask"></i> SQLi · XSS · Crypto
                    <span class="tag"><i class="fas fa-check-circle" style="color:#3fb950;"></i> Completed</span>
                </div>
            </div>
        </div>

        <!-- ===== PROJECTS ===== -->
        <div class="section-title">
            <i class="fas fa-folder-open"></i> Featured Projects
        </div>
        <div class="card-grid">
            <div class="card">
                <div class="card-icon"><i class="fas fa-fish"></i></div>
                <h3>Phishing Detection Tool</h3>
                <p>ML‑based URL classifier with browser extension · Real‑time threat detection</p>
                <div class="meta">
                    <i class="fas fa-code-branch"></i> Python · ML · Browser Ext
                    <span class="tag">Feb–May 2025</span>
                </div>
            </div>
            <div class="card">
                <div class="card-icon"><i class="fas fa-network-wired"></i></div>
                <h3>Network Services 2</h3>
                <p>TryHackMe walkthrough — enumeration, exploitation &amp; privilege escalation</p>
                <div class="meta">
                    <i class="fas fa-terminal"></i> THM · Network Pentesting
                    <span class="tag"><i class="fas fa-check-circle" style="color:#3fb950;"></i> Completed</span>
                </div>
            </div>
            <div class="card">
                <div class="card-icon"><i class="fas fa-robot"></i></div>
                <h3>AI Prompt Injection Lab</h3>
                <p>Jailbreaking &amp; prompt injection — VERA concierge exploitation</p>
                <div class="meta">
                    <i class="fas fa-brain"></i> AI Security · OWASP LLM
                    <span class="tag"><i class="fas fa-flask"></i> Lab</span>
                </div>
            </div>
        </div>

        <!-- ===== STATS ===== -->
        <div class="section-title" style="margin-top: 28px;">
            <i class="fas fa-chart-simple"></i> GitHub Analytics
        </div>
        <div class="stats-row">
            <div class="stat-item">
                <i class="fas fa-code-fork"></i>
                <span class="num">12</span>
                <span class="lbl">Repos</span>
            </div>
            <div class="stat-item">
                <i class="fas fa-star"></i>
                <span class="num">28</span>
                <span class="lbl">Stars</span>
            </div>
            <div class="stat-item">
                <i class="fas fa-code"></i>
                <span class="num">1.2k</span>
                <span class="lbl">Commits</span>
            </div>
            <div class="stat-item">
                <i class="fas fa-user-friends"></i>
                <span class="num">14</span>
                <span class="lbl">Followers</span>
            </div>
            <div class="stat-item">
                <i class="fas fa-trophy"></i>
                <span class="num">3</span>
                <span class="lbl">Achievements</span>
            </div>
        </div>

        <!-- ===== CONTRIBUTION HEATMAP (animated mock) ===== -->
        <div style="margin: 8px 0 4px 0;">
            <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:8px;">
                <span style="font-size:0.85rem; color:#8b949e;">
                    <i class="fas fa-calendar-alt" style="color:#58a6ff;"></i> 2026 Contribution Activity
                </span>
                <span style="font-size:0.75rem; color:#8b949e;">🔥 1,287 contributions</span>
            </div>
            <div class="heatmap" id="heatmapContainer">
                <!-- JavaScript will fill this -->
            </div>
            <div class="heatmap-legend">
                <span>Less</span>
                <span class="swatch"></span>
                <span class="swatch l1"></span>
                <span class="swatch l2"></span>
                <span class="swatch l3"></span>
                <span class="swatch l4"></span>
                <span class="swatch l5"></span>
                <span>More</span>
            </div>
        </div>

        <!-- ===== FOOTER ===== -->
        <div class="footer-note">
            <i class="fas fa-heart"></i>
            Built with <span style="color:#58a6ff;">passion</span> for cybersecurity &amp; open source &nbsp;·&nbsp;
            <i class="fas fa-code"></i> Gopikrishnan S &nbsp;·&nbsp;
            <i class="fas fa-flag"></i> #CyberSecurityJourney
        </div>

    </div>

    <script>
        // ============================================================
        //  1. TYPING EFFECT
        // ============================================================
        const phrases = [
            'Ethical Hacking',
            'Penetration Testing',
            'CTF Player',
            'TryHackMe Top 3%',
            'Security Researcher',
            'Red Teaming',
            'Web App Security',
            'Digital Forensics'
        ];

        let idx = 0,
            charIdx = 0,
            isDeleting = false;
        const el = document.getElementById('typingText');

        function typeLoop() {
            const current = phrases[idx];
            if (!isDeleting) {
                el.textContent = current.slice(0, charIdx + 1);
                charIdx++;
                if (charIdx === current.length) {
                    isDeleting = true;
                    setTimeout(typeLoop, 1800);
                    return;
                }
                setTimeout(typeLoop, 70);
            } else {
                el.textContent = current.slice(0, charIdx - 1);
                charIdx--;
                if (charIdx === 0) {
                    isDeleting = false;
                    idx = (idx + 1) % phrases.length;
                    setTimeout(typeLoop, 400);
                    return;
                }
                setTimeout(typeLoop, 40);
            }
        }
        typeLoop();

        // ============================================================
        //  2. HEATMAP (52 columns × 7 rows = 364 cells)
        // ============================================================
        const container = document.getElementById('heatmapContainer');
        const levels = ['', 'l1', 'l2', 'l3', 'l4', 'l5'];

        function getLevel() {
            const r = Math.random();
            if (r < 0.30) return 0;
            if (r < 0.55) return 1;
            if (r < 0.75) return 2;
            if (r < 0.88) return 3;
            if (r < 0.96) return 4;
            return 5;
        }

        // Build 52×7 grid (364 cells) – each gets a random level
        for (let i = 0; i < 364; i++) {
            const cell = document.createElement('div');
            cell.className = 'day';
            const lvl = getLevel();
            if (lvl > 0) cell.classList.add('l' + lvl);
            // small additional randomness: some days are extra bright
            if (Math.random() < 0.04) cell.classList.add('l5');
            container.appendChild(cell);
        }

        // ============================================================
        //  3. SMOOTH SCROLL / HOVER GLOW (optional)
        // ============================================================
        document.querySelectorAll('.card, .skill-pill, .badge-item').forEach(el => {
            el.addEventListener('mouseenter', function() {
                this.style.transition = 'all 0.25s ease';
            });
        });

        console.log('🔥 Gopikrishnan S — animated README loaded!');
    </script>

</body>
</html>
