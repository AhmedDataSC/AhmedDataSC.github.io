<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name | Data Scientist</title>
    <link rel="stylesheet" href="style.css">
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#resume">Resume</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Home Section -->
    <section id="home" class="section">
        <div class="home-content">
            <img src="your-photo.jpg" alt="Your Name" class="profile-photo">
            <h1>Hi, I'm [Your Name]</h1>
            <p>Data Scientist passionate about turning raw data into actionable insights.</p>
            <div class="cta-buttons">
                <a href="#projects" class="btn">View Projects</a>
                <a href="#contact" class="btn">Contact Me</a>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <!-- Project 1 -->
            <div class="project-card">
                <img src="project1-thumbnail.jpg" alt="Project 1">
                <h3>Customer Churn Prediction</h3>
                <p>Built a model to predict customer churn using XGBoost (95% accuracy).</p>
                <a href="https://github.com/yourusername/project1" target="_blank" class="btn">View Code</a>
            </div>
            <!-- Add more project cards -->
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section">
        <h2>Technical Skills</h2>
        <div class="skills-list">
            <div class="skill-category">
                <h3>Languages</h3>
                <p>Python, SQL, R</p>
            </div>
            <div class="skill-category">
                <h3>Machine Learning</h3>
                <p>Scikit-learn, TensorFlow, PyTorch</p>
            </div>
            <!-- Add more categories -->
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <h2>Get in Touch</h2>
        <div class="contact-links">
            <a href="mailto:youremail@domain.com" class="btn"><i class="fas fa-envelope"></i> Email</a>
            <a href="https://linkedin.com/in/yourprofile" target="_blank" class="btn"><i class="fab fa-linkedin"></i> LinkedIn</a>
            <a href="https://github.com/yourusername" target="_blank" class="btn"><i class="fab fa-github"></i> GitHub</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2023 Your Name. All rights reserved.</p>
    </footer>
</body>
</html>

body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

nav {
    background: #333;
    padding: 1rem;
    position: fixed;
    width: 100%;
    top: 0;
}

nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 2rem;
}

nav a {
    color: white;
    text-decoration: none;
}

.section {
    padding: 4rem 2rem;
    min-height: 100vh;
    text-align: center;
}

.profile-photo {
    width: 200px;
    border-radius: 50%;
    margin: 1rem;
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    padding: 2rem;
}

.project-card {
    border: 1px solid #ddd;
    padding: 1rem;
    border-radius: 8px;
}

.btn {
    display: inline-block;
    padding: 0.5rem 1rem;
    background: #007bff;
    color: white;
    text-decoration: none;
    border-radius: 4px;
    margin: 0.5rem;
}
