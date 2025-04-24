<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmed Raza Ansari | Data Scientist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* CSS Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            background-color: #f5f5f5;
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
            gap: 2rem;
            margin: 0;
            padding: 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        .section {
            padding: 6rem 2rem 2rem;
            min-height: 100vh;
            text-align: center;
        }

        .profile-photo {
            width: 200px;
            border-radius: 50%;
            margin: 1rem;
            border: 4px solid #2c3e50;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 2rem;
        }

        .project-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .btn {
            display: inline-block;
            padding: 0.5rem 1.5rem;
            background: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 25px;
            margin: 0.5rem;
            transition: 0.3s;
        }

        .btn:hover {
            background: #2980b9;
        }

        .certification-card {
            background: white;
            padding: 1rem;
            margin: 1rem auto;
            max-width: 600px;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
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

    <!-- Home Section -->
    <section id="home" class="section">
        <div class="home-content">
            <img src="your-photo.jpg" alt="Ahmed Raza Ansari" class="profile-photo">
            <h1>Ahmed Raza Ansari</h1>
            <p>Data Science Enthusiast | Fresh Graduate | Transforming Data into Insights</p>
            <div class="cta-buttons">
                <a href="#projects" class="btn">View Projects</a>
                <a href="#contact" class="btn">Hire Me</a>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>My Projects</h2>
        <div class="project-grid">
            <!-- Project 1 -->
            <div class="project-card">
                <h3>Customer Churn Prediction</h3>
                <p>Developed a machine learning model to predict customer churn using Logistic Regression.</p>
                <p>📊 Tech Stack: Python, Pandas, Scikit-learn</p>
                <a href="https://github.com/AhmedDataSC/project1" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Code
                </a>
            </div>

            <!-- Project 2 -->
            <div class="project-card">
                <h3>Sales Data Analysis</h3>
                <p>Performed EDA and created interactive dashboards to analyze sales trends.</p>
                <p>📈 Tech Stack: Python, Matplotlib, Tableau</p>
                <a href="https://github.com/AhmedDataSC/project2" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Code
                </a>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <h2>Technical Skills</h2>
        <div class="skills-list">
            <div class="certification-card">
                <h3>Programming</h3>
                <p>Python | SQL | R</p>
            </div>
            <div class="certification-card">
                <h3>Data Analysis</h3>
                <p>Pandas | NumPy | Excel</p>
            </div>
            <div class="certification-card">
                <h3>Machine Learning</h3>
                <p>Scikit-learn | TensorFlow</p>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section id="certifications" class="section">
        <h2>Certifications</h2>
        <div class="certification-card">
            <h3>Data Science Professional Certificate</h3>
            <p>Coursera | Issued 2023</p>
            <a href="[Your_Certificate_Link]" class="btn" target="_blank">
                <i class="fas fa-certificate"></i> Verify Credential
            </a>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <h2>Let's Connect!</h2>
        <div class="contact-links">
            <a href="mailto:ahmedraza@email.com" class="btn">
                <i class="fas fa-envelope"></i> Email
            </a>
            <a href="https://linkedin.com/in/yourprofile" class="btn" target="_blank">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
            <a href="https://github.com/AhmedDataSC" class="btn" target="_blank">
                <i class="fab fa-github"></i> GitHub
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer style="background: #2c3e50; color: white; text-align: center; padding: 1rem;">
        <p>© 2023 Ahmed Raza Ansari. All rights reserved.</p>
    </footer>
</body>
</html>
