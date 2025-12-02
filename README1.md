<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Waqar Ishaq — AI Developer & ML Engineer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #00d4ff;
            --primary-dark: #0099cc;
            --secondary: #7b61ff;
            --dark-bg: #0a0a0f;
            --card-bg: #13131f;
            --card-border: #222233;
            --text-light: #f0f0f5;
            --text-muted: #a0a0c0;
            --gradient: linear-gradient(135deg, #00d4ff 0%, #7b61ff 100%);
            --glow: 0 0 20px rgba(0, 212, 255, 0.3);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--dark-bg);
            color: var(--text-light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Smooth scroll */
        html {
            scroll-behavior: smooth;
        }
        
        /* Header with animated gradient */
        header {
            background: linear-gradient(135deg, rgba(10, 10, 15, 0.95) 0%, rgba(19, 19, 31, 0.9) 100%), 
                        url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiB2aWV3Qm94PSIwIDAgMTAwIDEwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48ZGVmcz48cGF0dGVybiBpZD0iZ3JpZCIgd2lkdGg9IjQwIiBoZWlnaHQ9IjQwIiBwYXR0ZXJuVW5pdHM9InVzZXJTcGFjZU9uVXNlIj48cGF0aCBkPSJNIDQwIDAgTCAwIDAgMCA0MCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjMDAyYzQ5IiBzdHJva2Utd2lkdGg9IjAuNSIvPjwvcGF0dGVybj48L2RlZnM+PHJlY3Qgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgZmlsbD0idXJsKCNncmlkKSIvPjwvc3ZnPg==');
            padding: 40px 20px 60px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: var(--gradient);
            opacity: 0.1;
            filter: blur(60px);
            z-index: -1;
            animation: rotate 20s linear infinite;
        }
        
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .profile-container {
            position: relative;
            display: inline-block;
            margin-bottom: 20px;
        }
        
        header img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 4px solid transparent;
            object-fit: cover;
            background: linear-gradient(white, white) padding-box,
                        var(--gradient) border-box;
            box-shadow: var(--glow);
            transition: transform 0.5s ease, box-shadow 0.5s ease;
        }
        
        header img:hover {
            transform: scale(1.05);
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
        }
        
        .profile-glow {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: var(--gradient);
            filter: blur(15px);
            opacity: 0.5;
            z-index: -1;
            animation: pulse 3s infinite alternate;
        }
        
        @keyframes pulse {
            0% { opacity: 0.3; }
            100% { opacity: 0.7; }
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 8px;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
            letter-spacing: -0.5px;
        }
        
        .tagline {
            font-size: 1.3rem;
            color: var(--text-muted);
            margin-bottom: 20px;
            font-weight: 300;
        }
        
        .header-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 25px;
            flex-wrap: wrap;
        }
        
        .header-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 12px 25px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 50px;
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }
        
        .header-btn:hover {
            background: var(--gradient);
            transform: translateY(-3px);
            box-shadow: var(--glow);
            border-color: transparent;
        }
        
        .header-btn.linkedin {
            background: rgba(10, 102, 194, 0.2);
            border-color: rgba(10, 102, 194, 0.3);
        }
        
        .header-btn.github {
            background: rgba(24, 23, 23, 0.2);
            border-color: rgba(255, 255, 255, 0.1);
        }
        
        .header-btn.hire-me {
            background: rgba(123, 97, 255, 0.2);
            border-color: rgba(123, 97, 255, 0.3);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: -30px auto 40px;
            position: relative;
            z-index: 2;
        }
        
        .section {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 20px;
            margin-bottom: 30px;
            border: 1px solid var(--card-border);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3), var(--glow);
        }
        
        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: var(--gradient);
        }
        
        h2 {
            margin-top: 0;
            color: var(--primary);
            font-size: 1.8rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        h2 i {
            color: var(--secondary);
        }
        
        p {
            color: var(--text-muted);
            font-size: 1.05rem;
            line-height: 1.8;
        }
        
        .highlight {
            color: var(--primary);
            font-weight: 600;
        }
        
        .skills-grid, .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .skill, .project {
            background: rgba(0, 0, 0, 0.2);
            padding: 18px 20px;
            border-radius: 12px;
            font-weight: 500;
            border-left: 4px solid var(--primary);
            transition: all 0.3s ease;
            cursor: default;
            position: relative;
            overflow: hidden;
        }
        
        .skill:hover, .project:hover {
            background: rgba(0, 212, 255, 0.1);
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .skill::before, .project::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }
        
        .skill:hover::before, .project:hover::before {
            left: 100%;
        }
        
        .project {
            border-left-color: var(--secondary);
        }
        
        .contact {
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .contact p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact i {
            color: var(--primary);
            width: 24px;
        }
        
        footer {
            text-align: center;
            padding: 30px 20px;
            color: var(--text-muted);
            border-top: 1px solid var(--card-border);
            background: var(--card-bg);
            margin-top: 50px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--card-bg);
            color: var(--text-light);
            font-size: 1.2rem;
            transition: all 0.3s ease;
            border: 1px solid var(--card-border);
        }
        
        .social-links a:hover {
            background: var(--gradient);
            color: white;
            transform: translateY(-5px);
            box-shadow: var(--glow);
        }
        
        .social-links a.linkedin:hover {
            background: #0A66C2;
        }
        
        .social-links a.github:hover {
            background: #333;
        }
        
        /* Floating animation for some elements */
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        /* Stats section */
        .stats {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .stat-item {
            text-align: center;
            flex: 1;
            min-width: 150px;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 5px;
        }
        
        .stat-label {
            color: var(--text-muted);
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .skills-grid, .project-grid {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.1rem;
            }
            
            header img {
                width: 150px;
                height: 150px;
            }
            
            .header-links {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }
            
            .header-btn {
                width: 80%;
                justify-content: center;
            }
        }
        
        @media (max-width: 480px) {
            .skills-grid, .project-grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .section {
                padding: 20px;
            }
            
            .stat-item {
                min-width: 120px;
            }
        }
        
        /* Certificate styling */
        ul {
            list-style: none;
            padding-left: 0;
        }
        
        ul li {
            padding: 10px 0;
            color: var(--text-muted);
            border-bottom: 1px dashed var(--card-border);
            position: relative;
            padding-left: 30px;
        }
        
        ul li:last-child {
            border-bottom: none;
        }
        
        ul li::before {
            content: '\f19d';
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            color: var(--primary);
            position: absolute;
            left: 0;
        }
        
        /* Scroll progress bar */
        .scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            width: 0%;
            height: 4px;
            background: var(--gradient);
            z-index: 9999;
            transition: width 0.1s ease;
        }
        
        /* Quick contact buttons */
        .quick-contact {
            display: flex;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .contact-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 10px 20px;
            background: rgba(0, 212, 255, 0.1);
            border: 1px solid rgba(0, 212, 255, 0.2);
            border-radius: 8px;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .contact-btn:hover {
            background: rgba(0, 212, 255, 0.2);
            transform: translateY(-3px);
        }
        
        .contact-btn.hire {
            background: rgba(123, 97, 255, 0.2);
            border-color: rgba(123, 97, 255, 0.3);
            color: #b5a8ff;
        }
        
        .hire-section {
            text-align: center;
            background: linear-gradient(135deg, rgba(123, 97, 255, 0.05), rgba(0, 212, 255, 0.05));
            border: 2px dashed var(--secondary);
        }
        
        .hire-section h2 {
            justify-content: center;
        }
    </style>
</head>
<body>
    <div class="scroll-progress"></div>
    
    <header>
        <div class="profile-container">
            <div class="profile-glow"></div>
            <!-- **YOUR PROFILE PICTURE ADDED HERE** -->
            <img src="profile picture.png" alt="Waqar Ishaq" />
        </div>
        <h1 class="floating">Waqar Ishaq</h1>
        <div class="tagline">AI Developer • ML Engineer • Full Stack with AI</div>
        
        <div class="header-links">
            <a href="https://www.linkedin.com/in/waqar-ali-15aa27280/" target="_blank" class="header-btn linkedin">
                <i class="fab fa-linkedin-in"></i> LinkedIn Profile
            </a>
            <a href="https://github.com/WAQARALI660" target="_blank" class="header-btn github">
                <i class="fab fa-github"></i> GitHub Portfolio
            </a>
            <a href="mailto:waqar.dev.codes@gmail.com" class="header-btn hire-me">
                <i class="fas fa-briefcase"></i> Hire Me
            </a>
        </div>
    </header>

    <div class="container">
        <!-- Stats Section -->
        <div class="section">
            <div class="stats">
                <div class="stat-item">
                    <div class="stat-number">15+</div>
                    <div class="stat-label">Projects Completed</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">10+</div>
                    <div class="stat-label">AI/ML Models</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">5+</div>
                    <div class="stat-label">Certifications</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Passionate</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-user"></i> About Me</h2>
            <p>
                I am a passionate AI Developer and Machine Learning Engineer with strong expertise in
                deep learning, LLMs, model fine‑tuning, data analytics, and building AI‑powered apps.
                I have completed <span class="highlight">Full Stack with AI</span> from NextSkill (Arfa Kareem Tower) and IT University.
                I love building intelligent systems like AI assistants, chatbots, and ML tools that solve real-world problems.
            </p>
            
            <div class="quick-contact">
                <a href="mailto:waqar.dev.codes@gmail.com" class="contact-btn">
                    <i class="fas fa-envelope"></i> Email Me
                </a>
                <a href="tel:+923134511629" class="contact-btn">
                    <i class="fas fa-phone"></i> Call Me
                </a>
                <a href="https://github.com/WAQARALI660" target="_blank" class="contact-btn">
                    <i class="fab fa-github"></i> View Projects
                </a>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-brain"></i> Core AI Skills</h2>
            <div class="skills-grid">
                <div class="skill">Machine Learning</div>
                <div class="skill">Deep Learning</div>
                <div class="skill">LLMs / Generative AI</div>
                <div class="skill">HuggingFace Models</div>
                <div class="skill">Model Fine‑Tuning</div>
                <div class="skill">AI Chatbots</div>
                <div class="skill">AI Assistants</div>
                <div class="skill">Computer Vision</div>
                <div class="skill">Data Cleaning</div>
                <div class="skill">Data Analytics</div>
                <div class="skill">Streamlit Apps</div>
                <div class="skill">Flask APIs</div>
                <div class="skill">FastAPI</div>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-code"></i> Python & ML Libraries</h2>
            <div class="skills-grid">
                <div class="skill">NumPy</div>
                <div class="skill">Pandas</div>
                <div class="skill">Seaborn</div>
                <div class="skill">Matplotlib</div>
                <div class="skill">Plotly</div>
                <div class="skill">Scikit‑Learn</div>
                <div class="skill">TensorFlow / Keras</div>
                <div class="skill">PyTorch</div>
                <div class="skill">OpenCV</div>
                <div class="skill">NLTK / SpaCy</div>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-project-diagram"></i> Projects</h2>
            <div class="project-grid">
                <div class="project">Image Classification Model</div>
                <div class="project">House Price Prediction</div>
                <div class="project">Step Counter AI App</div>
                <div class="project">Word Cloud Generator App</div>
                <div class="project">Real-time Object Detection</div>
                <div class="project">LLM-powered Chat Assistant</div>
            </div>
            <p style="margin-top: 15px; text-align: center;">
                <a href="https://github.com/WAQARALI660" target="_blank" style="color: var(--primary); text-decoration: none;">
                    <i class="fab fa-github"></i> View all projects on GitHub →
                </a>
            </p>
        </div>

        <div class="section">
            <h2><i class="fas fa-certificate"></i> Certificates</h2>
            <ul>
                <li>Full Stack with AI — NextSkill (Arfa Kareem Tower)</li>
                <li>Artificial Intelligence — IT University</li>
                <li>Deep Learning Specialization — DeepLearning.AI</li>
                <li>Machine Learning A-Z — Udemy</li>
            </ul>
        </div>

        <!-- Hire Me Section -->
        <div class="section hire-section">
            <h2><i class="fas fa-briefcase"></i> Available for Opportunities</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto;">
                I am actively seeking AI/ML development roles, internships, or freelance projects. 
                With strong skills in machine learning, deep learning, and AI application development, 
                I'm ready to contribute to innovative projects.
            </p>
            <div class="quick-contact" style="justify-content: center; margin-top: 25px;">
                <a href="mailto:waqar.dev.codes@gmail.com?subject=AI/ML Opportunity" class="contact-btn hire">
                    <i class="fas fa-paper-plane"></i> Send Opportunity
                </a>
                <a href="Waqar_Ishaq_Resume.pdf" download class="contact-btn">
                    <i class="fas fa-download"></i> Download Resume
                </a>
            </div>
        </div>

        <div class="section contact">
            <h2><i class="fas fa-envelope"></i> Contact</h2>
            <p><i class="fas fa-envelope"></i> <strong>Email:</strong> waqar.dev.codes@gmail.com</p>
            <p><i class="fas fa-phone"></i> <strong>Phone:</strong> 0313‑4511629</p>
            <p><i class="fas fa-map-marker-alt"></i> <strong>Location:</strong> Lahore, Pakistan</p>
            
            <h3 style="margin-top: 25px; margin-bottom: 15px; color: var(--text-light);">Connect with me</h3>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/waqar-ali-15aa27280/" target="_blank" title="LinkedIn" class="linkedin">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://github.com/WAQARALI660" target="_blank" title="GitHub" class="github">
                    <i class="fab fa-github"></i>
                </a>
                <a href="mailto:waqar.dev.codes@gmail.com" title="Email">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="tel:+923134511629" title="Call">
                    <i class="fas fa-phone"></i>
                </a>
            </div>
        </div>
    </div>

    <footer>
        © 2025 Waqar Ishaq — AI Developer Portfolio
        <div class="social-links">
            <a href="https://github.com/WAQARALI660" target="_blank" class="github">
                <i class="fab fa-github"></i>
            </a>
            <a href="https://www.linkedin.com/in/waqar-ali-15aa27280/" target="_blank" class="linkedin">
                <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="mailto:waqar.dev.codes@gmail.com">
                <i class="fas fa-envelope"></i>
            </a>
            <a href="tel:+923134511629">
                <i class="fas fa-phone"></i>
            </a>
        </div>
        <p style="margin-top: 15px; font-size: 0.9rem;">
            <a href="mailto:waqar.dev.codes@gmail.com" style="color: var(--primary); text-decoration: none;">
                waqar.dev.codes@gmail.com
            </a> | 0313‑4511629 | Open to AI/ML Opportunities
        </p>
    </footer>

    <script>
        // Scroll progress bar
        window.addEventListener('scroll', () => {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.querySelector('.scroll-progress').style.width = scrolled + '%';
        });
        
        // Add animation to sections when they come into view
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        // Observe all sections
        document.querySelectorAll('.section').forEach((section) => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            section.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            observer.observe(section);
        });
        
        // Skill hover effect enhancement
        document.querySelectorAll('.skill, .project').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.zIndex = '10';
            });
            
            item.addEventListener('mouseleave', function() {
                this.style.zIndex = '1';
            });
        });
        
        // Animate stats counter
        function animateStats() {
            const statNumbers = document.querySelectorAll('.stat-number');
            
            statNumbers.forEach(stat => {
                const target = stat.textContent.includes('+') ? 
                    parseInt(stat.textContent) : 
                    (stat.textContent === '100%' ? 100 : 0);
                
                let current = 0;
                const increment = target / 50;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        current = target;
                        clearInterval(timer);
                    }
                    if (stat.textContent.includes('+')) {
                        stat.textContent = Math.floor(current) + '+';
                    } else if (stat.textContent.includes('%')) {
                        stat.textContent = Math.floor(current) + '%';
                    }
                }, 30);
            });
        }
        
        // Trigger stats animation when section is in view
        const statsSection = document.querySelector('.section');
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateStats();
                    statsObserver.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });
        
        if (statsSection) {
            statsObserver.observe(statsSection);
        }
        
        // Add click-to-copy email
        const emailElement = document.querySelector('a[href^="mailto"]');
        if (emailElement) {
            emailElement.addEventListener('click', function(e) {
                // Allow default mailto behavior
                // Optional: Add copy to clipboard feature
                // navigator.clipboard.writeText('waqar.dev.codes@gmail.com');
            });
        }
    </script>
</body>
</html>