<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TRIANA115.exe // SYSTEM ONLINE</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon-cyan: #00ffff;
            --neon-pink: #ff0080;
            --neon-purple: #8a2be2;
            --neon-green: #39ff14;
            --dark-bg: #0a0a0a;
            --darker-bg: #050505;
            --grid-color: rgba(0, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Rajdhani', sans-serif;
            background: var(--dark-bg);
            color: var(--neon-cyan);
            overflow-x: hidden;
            position: relative;
        }

        /* Animated Background Grid */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 255, 255, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 255, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: gridMove 20s linear infinite;
            z-index: -1;
        }

        @keyframes gridMove {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Glitch Effect for Main Title */
        .glitch {
            font-family: 'Orbitron', monospace;
            font-size: 3rem;
            font-weight: 900;
            text-align: center;
            margin: 2rem 0;
            position: relative;
            color: var(--neon-cyan);
            text-shadow: 
                0 0 5px var(--neon-cyan),
                0 0 10px var(--neon-cyan),
                0 0 15px var(--neon-cyan),
                0 0 20px var(--neon-cyan);
        }

        .glitch::before,
        .glitch::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .glitch::before {
            animation: glitch-1 0.5s infinite;
            color: var(--neon-pink);
            z-index: -1;
        }

        .glitch::after {
            animation: glitch-2 0.5s infinite;
            color: var(--neon-green);
            z-index: -2;
        }

        @keyframes glitch-1 {
            0%, 14%, 15%, 49%, 50%, 99%, 100% { transform: translate(0); }
            15%, 49% { transform: translate(-2px, -1px); }
        }

        @keyframes glitch-2 {
            0%, 20%, 21%, 62%, 63%, 99%, 100% { transform: translate(0); }
            21%, 62% { transform: translate(2px, 1px); }
        }

        /* Neon Boxes */
        .neon-box {
            background: rgba(0, 0, 0, 0.8);
            border: 2px solid var(--neon-cyan);
            border-radius: 10px;
            padding: 2rem;
            margin: 2rem 0;
            box-shadow: 
                0 0 20px rgba(0, 255, 255, 0.3),
                inset 0 0 20px rgba(0, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .neon-box::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 255, 0.2), transparent);
            animation: scan 3s infinite;
        }

        @keyframes scan {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        /* ASCII Art Header */
        .ascii-art {
            font-family: 'Orbitron', monospace;
            font-size: 0.8rem;
            line-height: 1.2;
            color: var(--neon-cyan);
            text-align: center;
            margin: 2rem 0;
            white-space: pre;
            text-shadow: 0 0 10px var(--neon-cyan);
        }

        /* Typing Animation */
        .typing-text {
            font-family: 'Orbitron', monospace;
            font-size: 1.5rem;
            text-align: center;
            margin: 2rem 0;
            color: var(--neon-green);
            text-shadow: 0 0 10px var(--neon-green);
        }

        /* Progress Bars */
        .progress-container {
            margin: 1rem 0;
        }

        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .progress-bar {
            width: 100%;
            height: 20px;
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid var(--neon-cyan);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--neon-cyan), var(--neon-pink));
            border-radius: 10px;
            animation: pulse 2s infinite;
            position: relative;
        }

        .progress-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: shimmer 1.5s infinite;
        }

        @keyframes pulse {
            0%, 100% { box-shadow: 0 0 5px var(--neon-cyan); }
            50% { box-shadow: 0 0 20px var(--neon-cyan), 0 0 30px var(--neon-cyan); }
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Tech Stack Badges */
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin: 2rem 0;
        }

        .tech-badge {
            padding: 0.5rem 1rem;
            background: rgba(0, 0, 0, 0.8);
            border: 2px solid var(--neon-pink);
            border-radius: 25px;
            color: var(--neon-pink);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .tech-badge:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(255, 0, 128, 0.4);
            color: white;
            background: var(--neon-pink);
        }

        .tech-badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }

        .tech-badge:hover::before {
            left: 100%;
        }

        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .stat-card {
            background: rgba(0, 0, 0, 0.9);
            border: 2px solid var(--neon-purple);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
            box-shadow: 0 0 30px rgba(138, 43, 226, 0.5);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 900;
            color: var(--neon-purple);
            text-shadow: 0 0 20px var(--neon-purple);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1.2rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* Terminal Window */
        .terminal {
            background: rgba(0, 0, 0, 0.95);
            border: 2px solid var(--neon-green);
            border-radius: 10px;
            margin: 2rem 0;
            overflow: hidden;
            box-shadow: 0 0 30px rgba(57, 255, 20, 0.3);
        }

        .terminal-header {
            background: rgba(57, 255, 20, 0.1);
            padding: 1rem;
            border-bottom: 1px solid var(--neon-green);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .terminal-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--neon-green);
            box-shadow: 0 0 10px var(--neon-green);
        }

        .terminal-content {
            padding: 1.5rem;
            font-family: 'Orbitron', monospace;
            color: var(--neon-green);
            line-height: 1.6;
        }

        .terminal-line {
            margin: 0.5rem 0;
            animation: typewriter 2s steps(40) infinite;
        }

        @keyframes typewriter {
            0% { width: 0; }
            50% { width: 100%; }
            100% { width: 100%; }
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 3rem 0;
        }

        .social-link {
            width: 60px;
            height: 60px;
            border: 2px solid var(--neon-cyan);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--neon-cyan);
            text-decoration: none;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .social-link:hover {
            transform: rotate(360deg) scale(1.2);
            box-shadow: 0 0 30px var(--neon-cyan);
            border-color: var(--neon-pink);
            color: var(--neon-pink);
        }

        /* Footer */
        .footer {
            text-align: center;
            margin: 3rem 0;
            padding: 2rem 0;
            border-top: 1px solid rgba(0, 255, 255, 0.3);
        }

        .signature {
            font-family: 'Orbitron', monospace;
            font-size: 1.2rem;
            color: var(--neon-cyan);
            text-shadow: 0 0 15px var(--neon-cyan);
            margin: 1rem 0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .glitch {
                font-size: 2rem;
            }
            
            .ascii-art {
                font-size: 0.6rem;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .tech-stack {
                gap: 0.5rem;
            }
            
            .social-links {
                gap: 1rem;
            }
        }

        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: var(--darker-bg);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--neon-cyan);
            box-shadow: 0 0 10px var(--neon-cyan);
        }

        ::-webkit-scrollbar-thumb:hover {
            background: var(--neon-pink);
            box-shadow: 0 0 10px var(--neon-pink);
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="glitch" data-text="TRIANA115.exe">TRIANA115.exe</div>
        
        <div class="ascii-art">
╔══════════════════════════════════════════════════════════════════════════════╗
║  ████████╗██████╗ ██╗ █████╗ ███╗   ██╗ █████╗      ██╗ ██╗███████╗        ║
║  ╚══██╔══╝██╔══██╗██║██╔══██╗████╗  ██║██╔══██╗    ███║███║██╔════╝        ║
║     ██║   ██████╔╝██║███████║██╔██╗ ██║███████║    ╚██║╚██║███████╗        ║
║     ██║   ██╔══██╗██║██╔══██║██║╚██╗██║██╔══██║     ██║ ██║╚════██║        ║
║     ██║   ██║  ██║██║██║  ██║██║ ╚████║██║  ██║     ██║ ██║███████║        ║
║     ╚═╝   ╚═╝  ╚═╝╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝  ╚═╝     ╚═╝ ╚═╝╚══════╝        ║
║                                                                              ║
║  >> CYBERDECK INITIALIZED... WELCOME TO THE MATRIX <<                       ║
╚══════════════════════════════════════════════════════════════════════════════╝
        </div>

        <div class="typing-text" id="typingText">NEURAL INTERFACE ACTIVATED...</div>

        <!-- System Specifications -->
        <div class="neon-box">
            <h2 style="text-align: center; margin-bottom: 2rem; color: var(--neon-pink); text-shadow: 0 0 15px var(--neon-pink);">🔥 SYSTEM SPECIFICATIONS</h2>
            
            <div class="progress-container">
                <div class="progress-label">
                    <span>🧠 CORTEX LEVEL</span>
                    <span>89%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 89%;"></div>
                </div>
            </div>

            <div class="progress-container">
                <div class="progress-label">
                    <span>⚡ ENERGY CORE</span>
                    <span>92%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 92%;"></div>
                </div>
            </div>

            <div class="progress-container">
                <div class="progress-label">
                    <span>🔮 CREATIVITY</span>
                    <span>85%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 85%;"></div>
                </div>
            </div>

            <div class="progress-container">
                <div class="progress-label">
                    <span>🎯 FOCUS MODE</span>
                    <span>95%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 95%;"></div>
                </div>
            </div>

            <div class="progress-container">
                <div class="progress-label">
                    <span>🚀 INNOVATION</span>
                    <span>90%</span>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: 90%;"></div>
                </div>
            </div>
        </div>

        <!-- Tech Stack -->
        <div class="neon-box">
            <h2 style="text-align: center; margin-bottom: 2rem; color: var(--neon-green); text-shadow: 0 0 15px var(--neon-green);">🌐 NETWORK PROTOCOLS MASTERED</h2>
            <div class="tech-stack">
                <div class="tech-badge">JavaScript</div>
                <div class="tech-badge">Python</div>
                <div class="tech-badge">React</div>
                <div class="tech-badge">Node.js</div>
                <div class="tech-badge">MongoDB</div>
                <div class="tech-badge">Docker</div>
                <div class="tech-badge">HTML5</div>
                <div class="tech-badge">CSS3</div>
                <div class="tech-badge">Git</div>
                <div class="tech-badge">AI/ML</div>
            </div>
        </div>

        <!-- Stats -->
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-number" id="repos">127</div>
                <div class="stat-label">Repositories</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="commits">2.5K</div>
                <div class="stat-label">Commits</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="stars">456</div>
                <div class="stat-label">Stars</div>
            </div>
        </div>

        <!-- Terminal -->
        <div class="terminal">
            <div class="terminal-header">
                <div class="terminal-dot"></div>
                <div class="terminal-dot"></div>
                <div class="terminal-dot"></div>
                <span style="margin-left: 1rem; color: var(--neon-green);">TRIANA115@cyberdeck:~$</span>
            </div>
            <div class="terminal-content" id="terminalContent">
                <div class="terminal-line">> Initializing neural networks...</div>
                <div class="terminal-line">> Loading quantum algorithms...</div>
                <div class="terminal-line">> Connecting to the matrix...</div>
                <div class="terminal-line">> Status: FULLY OPERATIONAL</div>
                <div class="terminal-line">> Ready for digital adventures...</div>
            </div>
        </div>

        <!-- Mission Parameters -->
        <div class="neon-box">
            <h2 style="text-align: center; margin-bottom: 2rem; color: var(--neon-purple); text-shadow: 0 0 15px var(--neon-purple);">🔴 ACTIVE MISSION PARAMETERS</h2>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem;">
                <div>
                    <h3 style="color: var(--neon-cyan); margin-bottom: 1rem;">🎯 CURRENT QUEST</h3>
                    <ul style="list-style: none; color: var(--neon-green);">
                        <li>🚀 Building the future one algorithm at a time</li>
                        <li>🧠 Exploring AI/ML neural networks</li>
                        <li>✨ Crafting elegant user experiences</li>
                        <li>🌐 Creating digital solutions</li>
                    </ul>
                </div>
                <div>
                    <h3 style="color: var(--neon-cyan); margin-bottom: 1rem;">🧠 KNOWLEDGE STACK</h3>
                    <div class="progress-container">
                        <div class="progress-label"><span>Problem Solving</span><span>100%</span></div>
                        <div class="progress-bar"><div class="progress-fill" style="width: 100%;"></div></div>
                    </div>
                    <div class="progress-container">
                        <div class="progress-label"><span>Full-Stack Dev</span><span>85%</span></div>
                        <div class="progress-bar"><div class="progress-fill" style="width: 85%;"></div></div>
                    </div>
                    <div class="progress-container">
                        <div class="progress-label"><span>Cloud Architecture</span><span>78%</span></div>
                        <div class="progress-bar"><div class="progress-fill" style="width: 78%;"></div></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Social Links -->
        <div class="social-links">
            <a href="#" class="social-link" title="GitHub">🐙</a>
            <a href="#" class="social-link" title="LinkedIn">💼</a>
            <a href="#" class="social-link" title="Twitter">🐦</a>
            <a href="#" class="social-link" title="Portfolio">🌐</a>
            <a href="#" class="social-link" title="Email">📧</a>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="signature">
                >> SYSTEM SIGNATURE: TRIANA115.exe <<
            </div>
            <p>"The future belongs to those who understand the digital realm"</p>
            <p style="margin-top: 1rem; color: var(--neon-pink);">
                Made with 💜 and ⚡ in the Matrix
            </p>
        </div>
    </div>

    <script>
        // Typing animation
        const phrases = [
            "NEURAL INTERFACE ACTIVATED...",
            "CODE RUNNER | DIGITAL ARCHITECT",
            "BREAKING THE MATRIX ONE COMMIT AT A TIME",
            "SYSTEM STATUS: ONLINE"
        ];
        
        let currentPhrase = 0;
        let currentChar = 0;
        let isDeleting = false;
        
        function typeWriter() {
            const element = document.getElementById('typingText');
            const current = phrases[currentPhrase];
            
            if (isDeleting) {
                element.textContent = current.substring(0, currentChar - 1);
                currentChar--;
            } else {
                element.textContent = current.substring(0, currentChar + 1);
                currentChar++;
            }
            
            if (!isDeleting && currentChar === current.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && currentChar === 0) {
                isDeleting = false;
                currentPhrase = (currentPhrase + 1) % phrases.length;
            }
            
            setTimeout(typeWriter, isDeleting ? 50 : 100);
        }
        
        // Animate stats on scroll
        function animateStats() {
            const stats = document.querySelectorAll('.stat-number');
            stats.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 50;
                
                const updateStat = () => {
                    if (current < target) {
                        current += increment;
                        stat.textContent = Math.ceil(current).toLocaleString();
                        requestAnimationFrame(updateStat);
                    } else {
                        stat.textContent = target.toLocaleString();
                    }
                };
                
                updateStat();
            });
        }
        
        // Start animations
        typeWriter();
        animateStats();
        
        // Add glitch effect on hover
        document.addEventListener('mousemove', (e) => {
            const glitchElements = document.querySelectorAll('.glitch');
            glitchElements.forEach(element => {
                const rect = element.getBoundingClientRect();
                const distance = Math.sqrt(
                    Math.pow(e.clientX - (rect.left + rect.width / 2), 2) +
                    Math.pow(e.clientY - (rect.top + rect.height / 2), 2)
                );
                
                if (distance < 200) {
                    element.style.animation = 'glitch-1 0.3s infinite';
                } else {
                    element.style.animation = 'none';
                }
            });
        });
    </script>
</body>
</html>