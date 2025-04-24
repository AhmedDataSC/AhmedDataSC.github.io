<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmed Raza Ansari | Data Scientist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            background-color: #f8f9fa;
            color: #333;
        }

        nav {
            background: #2c3e50;
            padding: 1rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 1rem;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: 0.3s;
        }

        nav a:hover {
            background: #3498db;
        }

        .section {
            padding: 6rem 1.5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        h1, h2, h3 {
            color: #2c3e50;
            margin-bottom: 1.5rem;
        }

        .profile {
            text-align: center;
            padding: 2rem 0;
        }

        .profile-photo {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 4px solid #2c3e50;
            margin-bottom: 1.5rem;
            object-fit: cover;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            padding: 1rem 0;
        }

        .project-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            padding: 1rem 0;
        }

        .skill-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            padding: 1rem 0;
        }

        .certification-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.6rem 1.5rem;
            background: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 25px;
            margin: 0.5rem 0;
            transition: 0.3s;
            font-size: 0.9rem;
        }

        .btn:hover {
            background: #2980b9;
            transform: translateY(-2px);
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
            padding: 2rem 0;
        }

        @media (max-width: 768px) {
            .section {
                padding: 5rem 1rem 1rem;
            }

            nav ul {
                gap: 0.8rem;
            }

            nav a {
                font-size: 0.9rem;
                padding: 0.4rem 0.8rem;
            }

            .profile-photo {
                width: 140px;
                height: 140px;
            }

            h1 {
                font-size: 1.8rem;
            }

            h2 {
                font-size: 1.5rem;
            }
        }

        @media (max-width: 480px) {
            .project-grid,
            .certifications-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#certifications">Certifications</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home" class="section">
        <div class="profile">
            <img src="ahmed-photo.jpg" alt="Ahmed Raza Ansari" class="profile-photo">
            <h1>Ahmed Raza Ansari</h1>
            <p>Data Science Professional | AI Enthusiast</p>
            <div class="cta-buttons">
                <a href="#projects" class="btn">View Projects</a>
                <a href="#contact" class="btn">Contact Me</a>
            </div>
        </div>
    </section>

    <section id="projects" class="section">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <div class="project-card">
                <h3>Customer Churn Prediction</h3>
                <p>Built ML model with 92% accuracy using Python and Scikit-learn</p>
                <a href="https://github.com/AhmedDataSC/churn-prediction" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Code
                </a>
            </div>
            <div class="project-card">
                <h3>Sales Analytics Dashboard</h3>
                <p>Interactive Tableau dashboard for sales trend analysis</p>
                <a href="https://github.com/AhmedDataSC/sales-analytics" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Project
                </a>
            </div>
        </div>
    </section>

    <section id="skills" class="section">
        <h2>Technical Skills</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <h3>Data Science</h3>
                <p>Pandas • NumPy • Scikit-learn</p>
            </div>
            <div class="skill-card">
                <h3>Programming</h3>
                <p>Python • SQL • R</p>
            </div>
            <div class="skill-card">
                <h3>AI/ML</h3>
                <p>TensorFlow • Generative AI • NLP</p>
            </div>
        </div>
    </section>

    <section id="certifications" class="section">
        <h2>Certifications (2025)</h2>
        <div class="certifications-grid">
            <div class="certification-card">
                <h3>Advanced Data Science</h3>
                <p>Coursera • 2025</p>
                <a href="#" class="btn">View Credential</a>
            </div>
            <div class="certification-card">
                <h3>Python Programming</h3>
                <p>Coursera • 2025</p>
                <a href="#" class="btn">View Credential</a>
            </div>
            <div class="certification-card">
                <h3>Generative AI</h3>
                <p>Coursera • 2025</p>
                <a href="#" class="btn">View Credential</a>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <h2>Let's Connect</h2>
        <div class="contact-links">
            <a href="mailto:ahmed.ansari@example.com" class="btn">
                <i class="fas fa-envelope"></i> Email
            </a>
            <a href="https://www.linkedin.com/in/ahmed-raza-ansari-b442a2221" class="btn" target="_blank">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
            <a href="https://github.com/AhmedDataSC" class="btn" target="_blank">
                <i class="fab fa-github"></i> GitHub
            </a>
        </div>
    </section>

    <footer style="background: #2c3e50; color: white; text-align: center; padding: 1rem;">
        <p>© 2025 Ahmed Raza Ansari. All rights reserved.</p>
    </footer>
</body>
</html>
