# RASHIDUL-ISLAM-SHIFUL-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JP RASHIDUL | Senior Developer & Designer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-primary: #0a0f1d;
            --bg-secondary: #111827;
            --card-bg: rgba(30, 41, 59, 0.7);
            --accent: #38bdf8;
            --accent-glow: rgba(56, 189, 248, 0.3);
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --border-color: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-main);
            overflow-x: hidden;
        }

        #canvas-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        /* Navbar */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.2rem 8%;
            background: rgba(10, 15, 29, 0.85);
            backdrop-filter: blur(12px);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            border-bottom: 1px solid var(--border-color);
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 800;
            letter-spacing: 1.5px;
            color: #fff;
        }

        .logo span {
            color: var(--accent);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 10%;
            position: relative;
        }

        .badge {
            background: rgba(56, 189, 248, 0.1);
            color: var(--accent);
            border: 1px solid var(--accent-glow);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .typewriter {
            color: var(--accent);
            border-right: 3px solid var(--accent);
            animation: blink 0.7s infinite;
        }

        @keyframes blink { 50% { border-color: transparent; } }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            max-width: 650px;
            margin-bottom: 2.5rem;
        }

        .btn-group {
            display: flex;
            gap: 1.2rem;
        }

        .btn {
            padding: 0.9rem 2.2rem;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            transition: 0.3s ease;
            cursor: pointer;
        }

        .btn-primary {
            background: var(--accent);
            color: #000;
            box-shadow: 0 0 20px var(--accent-glow);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 30px var(--accent-glow);
        }

        .btn-outline {
            border: 1px solid var(--border-color);
            color: #fff;
            background: rgba(255, 255, 255, 0.05);
        }

        .btn-outline:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-3px);
        }

        /* Sections General */
        section {
            padding: 6rem 8%;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3.5rem;
            position: relative;
        }

        .section-title span {
            color: var(--accent);
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 2rem;
            border-radius: 12px;
            backdrop-filter: blur(8px);
            transition: 0.3s;
        }

        .skill-card:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
        }

        .skill-card i {
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .skill-card h3 {
            margin-bottom: 0.5rem;
        }

        .skill-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2.5rem;
            background: var(--bg-secondary);
            border-top: 1px solid var(--border-color);
            color: var(--text-muted);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1rem;
        }

        .social-links a {
            color: var(--text-muted);
            font-size: 1.5rem;
            transition: 0.3s;
        }

        .social-links a:hover {
            color: var(--accent);
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            nav ul { display: none; }
            .btn-group { flex-direction: column; }
        }
    </style>
</head>
<body>

    <canvas id="canvas-bg"></canvas>

    <!-- Header -->
    <header>
        <div class="logo">JP <span>RASHIDUL</span></div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="badge"><i class="fas fa-code"></i> Developer & Systems Integrator</div>
        <h1>Hi, I'm <span class="typewriter" id="typewriter-text"></span></h1>
        <p>Specializing in web application development, security bot architectures, and cloud services based in Japan.</p>
        <div class="btn-group">
            <a href="#contact" class="btn btn-primary">Contact Me</a>
            <a href="#skills" class="btn btn-outline">Explore Skills</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2 class="section-title">About <span>Me</span></h2>
        <div style="background: var(--card-bg); border: 1px solid var(--border-color); padding: 3rem; border-radius: 16px; max-width: 800px; margin: 0 auto; text-align: center; backdrop-filter: blur(10px);">
            <p style="font-size: 1.1rem; color: var(--text-muted); line-height: 1.8;">
                Welcome to my official domain. I build fast, secure, and modern digital platforms. From full-stack web engineering to automated bot integrations, I turn complex technical challenges into clean and reliable solutions.
            </p>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2 class="section-title">Technical <span>Expertise</span></h2>
        <div class="skills-grid">
            <div class="skill-card">
                <i class="fab fa-html5"></i>
                <h3>Web Development</h3>
                <p>HTML5, CSS3, JavaScript, and responsive modern frontend designs.</p>
            </div>
            <div class="skill-card">
                <i class="fab fa-node-js"></i>
                <h3>Backend & Bots</h3>
                <p>Node.js applications, automation bots, and system architecture.</p>
            </div>
            <div class="skill-card">
                <i class="fas fa-database"></i>
                <h3>Cloud & Authentication</h3>
                <p>Firebase Integration, GitHub deployment, and DNS management.</p>
            </div>
            <div class="skill-card">
                <i class="fas fa-shield-alt"></i>
                <h3>Security Systems</h3>
                <p>Moderation logic, server security, and API configurations.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2 class="section-title">Get In <span>Touch</span></h2>
        <div style="text-align: center; background: var(--card-bg); border: 1px solid var(--border-color); padding: 3rem; border-radius: 16px; max-width: 600px; margin: 0 auto;">
            <i class="fas fa-envelope" style="font-size: 3rem; color: var(--accent); margin-bottom: 1rem;"></i>
            <h3 style="margin-bottom: 1rem;">Let's Work Together</h3>
            <p style="color: var(--text-muted); margin-bottom: 1.5rem;">Feel free to reach out for projects, technical collaborations, or queries.</p>
            <a href="mailto:contact@rashiduljapan.com" class="btn btn-primary">contact@rashiduljapan.com</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-discord"></i></a>
            <a href="#"><i class="fas fa-globe"></i></a>
        </div>
        <p>&copy; 2026 JP RASHIDUL. All rights reserved.</p>
    </footer>

    <!-- Interactive Scripts -->
    <script>
        // Typing Effect
        const words = ["JP RASHIDUL", "a Web Developer", "a Systems Engineer"];
        let count = 0;
        let index = 0;
        let currentText = "";
        let letter = "";

        (function type() {
            if (count === words.length) count = 0;
            currentText = words[count];
            letter = currentText.slice(0, ++index);

            document.getElementById("typewriter-text").textContent = letter;
            if (letter.length === currentText.length) {
                count++;
                index = 0;
                setTimeout(type, 2000);
            } else {
                setTimeout(type, 100);
            }
        })();

        // Canvas Background Particles
        const canvas = document.getElementById('canvas-bg');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        let particlesArray = [];
        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 2 + 1;
                this.speedX = Math.random() * 1 - 0.5;
                this.speedY = Math.random() * 1 - 0.5;
            }
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                if (this.x > canvas.width) this.x = 0;
                if (this.x < 0) this.x = canvas.width;
                if (this.y > canvas.height) this.y = 0;
                if (this.y < 0) this.y = canvas.height;
            }
            draw() {
                ctx.fillStyle = 'rgba(56, 189, 248, 0.4)';
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function init() {
            particlesArray = [];
            for (let i = 0; i < 70; i++) particlesArray.push(new Particle());
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < particlesArray.length; i++) {
                particlesArray[i].update();
                particlesArray[i].draw();
            }
            requestAnimationFrame(animate);
        }

        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            init();
        });

        init();
        animate();
    </script>
</body>
</html>
