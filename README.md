<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmed Raza Ansari | Data Scientist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --text-color: #333;
            --bg-color: #f8f9fa;
            --card-bg: #ffffff;
        }

        /* Dark Mode Variables */
        [data-theme="dark"] {
            --primary-color: #3498db;
            --secondary-color: #2c3e50;
            --text-color: #f8f9fa;
            --bg-color: #1a1a1a;
            --card-bg: #2d2d2d;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            transition: all 0.3s ease;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            line-height: 1.6;
            background-color: var(--bg-color);
            color: var(--text-color);
        }

        /* Theme Toggle */
        .theme-toggle {
            position: fixed;
            top: 1rem;
            right: 1rem;
            cursor: pointer;
            z-index: 1001;
            background: var(--card-bg);
            padding: 0.5rem;
            border-radius: 50%;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        nav {
            background: var(--primary-color);
            padding: 1rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            font-weight: 500;
        }

        nav a:hover {
            background: var(--secondary-color);
        }

        .section {
            padding: 8rem 1.5rem 4rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .hero {
            text-align: center;
            padding: 4rem 0;
        }

        .profile-photo {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 4px solid var(--primary-color);
            margin-bottom: 2rem;
            object-fit: cover;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 2rem 0;
        }

        .project-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--secondary-color);
        }

        .skills-chart {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            padding: 2rem 0;
        }

        .skill-item {
            background: var(--card-bg);
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .skill-bar {
            height: 8px;
            background: #eee;
            border-radius: 4px;
            margin: 1rem 0;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: var(--secondary-color);
            width: 0;
            transition: width 1s ease-in-out;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section > * {
            animation: fadeIn 0.6s ease forwards;
        }

        @media (max-width: 768px) {
            .section {
                padding: 6rem 1rem 2rem;
            }

            nav ul {
                gap: 1rem;
            }

            .profile-photo {
                width: 160px;
                height: 160px;
            }
        }
    </style>
</head>
<body>
    <!-- Theme Toggle -->
    <div class="theme-toggle" onclick="toggleTheme()">
        <i class="fas fa-moon"></i>
    </div>

    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#certifications">Certifications</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="section">
        <div class="hero">
            <img src="https://github.com/AhmedDataSC.png" alt="Ahmed Raza Ansari" class="profile-photo">
            <h1 style="font-size: 2.5rem; margin-bottom: 1rem;">Ahmed Raza Ansari</h1>
            <p style="font-size: 1.2rem; color: var(--secondary-color);">Data Scientist | AI Developer</p>
            <div style="margin-top: 2rem;">
                <a href="#projects" class="btn" style="background: var(--secondary-color);">View Projects</a>
                <a href="#contact" class="btn" style="background: var(--primary-color);">Contact Me</a>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2 style="text-align: center; font-size: 2rem; margin-bottom: 3rem;">Featured Projects</h2>
        <div class="project-grid">
            <!-- Advanced House Price Prediction -->
            <div class="project-card">
                <h3>Advanced House Price Prediction</h3>
                <p style="margin: 1rem 0; color: #666;">Machine learning model predicting real estate prices with 95% accuracy</p>
                <div style="margin: 1.5rem 0;">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">TensorFlow</span>
                    <span class="tech-tag">EDA</span>
                </div>
                <a href="https://github.com/AhmedDataSC/Advanced-House-Price-Prediction" class="btn" target="_blank">
                    <i class="fab fa-github"></i> Explore Code
                </a>
            </div>

            <!-- Autoviz -->
            <div class="project-card">
                <h3>Autoviz</h3>
                <p style="margin: 1rem 0; color: #666;">Automated data visualization tool for rapid EDA</p>
                <div style="margin: 1.5rem 0;">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">Matplotlib</span>
                    <span class="tech-tag">Seaborn</span>
                </div>
                <a href="https://github.com/AhmedDataSC/Autoviz" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Project
                </a>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <h2 style="text-align: center; font-size: 2rem; margin-bottom: 3rem;">Technical Expertise</h2>
        <div class="skills-chart">
            <div class="skill-item">
                <h3>Machine Learning</h3>
                <div class="skill-bar">
                    <div class="skill-progress" style="width: 90%;"></div>
                </div>
                <p>Scikit-learn • TensorFlow • XGBoost</p>
            </div>
            
            <div class="skill-item">
                <h3>Data Analysis</h3>
                <div class="skill-bar">
                    <div class="skill-progress" style="width: 85%;"></div>
                </div>
                <p>Pandas • SQL • Power BI</p>
            </div>
            
            <div class="skill-item">
                <h3>Programming</h3>
                <div class="skill-bar">
                    <div class="skill-progress" style="width: 95%;"></div>
                </div>
                <p>Python • R • JavaScript</p>
            </div>
        </div>
    </section>

    <script>
        // Theme Toggle
        function toggleTheme() {
            const body = document.body;
            const themeToggle = document.querySelector('.theme-toggle i');
            
            if (body.getAttribute('data-theme') === 'dark') {
                body.removeAttribute('data-theme');
                themeToggle.className = 'fas fa-moon';
            } else {
                body.setAttribute('data-theme', 'dark');
                themeToggle.className = 'fas fa-sun';
            }
        }

        // Scroll Animation
        document.addEventListener('DOMContentLoaded', () => {
            const skillBars = document.querySelectorAll('.skill-progress');
            skillBars.forEach(bar => {
                const width = bar.style.width;
                bar.style.width = '0';
                setTimeout(() => {
                    bar.style.width = width;
                }, 500);
            });
        });

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
