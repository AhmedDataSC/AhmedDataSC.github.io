    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#certifications">Certifications</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="section">
        <div class="hero">
            <img src="https://github.com/AhmedDataSC.png" alt="Ahmed Raza Ansari" class="profile-photo">
            <h1>Ahmed Raza Ansari</h1>
            <p>Data Scientist | Machine Learning Engineer</p>
            <div style="margin-top: 2rem;">
                <a href="#projects" class="btn">View Projects</a>
                <a href="#contact" class="btn">Contact Me</a>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <div class="project-card">
                <h3>Advanced House Price Prediction</h3>
                <p>Machine learning model with 95% accuracy using advanced regression techniques</p>
                <div style="margin: 1rem 0;">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">TensorFlow</span>
                    <span class="tech-tag">Pandas</span>
                </div>
                <a href="https://github.com/AhmedDataSC/Advanced-House-Price-Prediction" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Project
                </a>
            </div>

            <div class="project-card">
                <h3>Autoviz</h3>
                <p>Automated data visualization system for exploratory data analysis</p>
                <div style="margin: 1rem 0;">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">Matplotlib</span>
                    <span class="tech-tag">Seaborn</span>
                </div>
                <a href="https://github.com/AhmedDataSC/Autoviz" class="btn" target="_blank">
                    <i class="fab fa-github"></i> View Code
                </a>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section id="certifications" class="section">
        <h2>Certifications</h2>
        <div class="certifications-grid">
            <div class="certification-card">
                <h3>Data Science Professional</h3>
                <p>Coursera | 2025</p>
                <div class="btn">View Credential</div>
            </div>
            <div class="certification-card">
                <h3>Advanced Python</h3>
                <p>Coursera | 2025</p>
                <div class="btn">View Credential</div>
            </div>
            <div class="certification-card">
                <h3>Generative AI</h3>
                <p>Coursera | 2025</p>
                <div class="btn">View Credential</div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <h2>Contact Me</h2>
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

    <!-- Fixed Footer -->
    <footer>
        <p>© 2025 Ahmed Raza Ansari. All rights reserved.</p>
    </footer>

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
