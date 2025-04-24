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
            min-height: 100vh;
            display: flex;
            flex-direction: column;
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

        .section {
            padding: 8rem 1.5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
            flex: 1;
        }

        .hero {
            text-align: center;
            padding: 4rem 0;
        }

        .profile-photo {
            width: 220px;
            height: 220px;
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

        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            padding: 2rem 0;
        }

        .certification-card {
            background: var(--card-bg);
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            text-align: center;
        }

        footer {
            background: var(--primary-color);
            color: white;
            text-align: center;
            padding: 1.5rem;
            margin-top: auto;
            position: static;
        }

        @media (max-width: 768px) {
            .section {
                padding: 6rem 1rem 2rem;
            }
            .profile-photo {
                width: 180px;
                height: 180px;
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
            <li><a href="#
