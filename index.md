<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Niharika MG | Cloud Engineer & Full-Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #e2e8f0;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            background: linear-gradient(45deg, #3b82f6, #8b5cf6);
            border-radius: 50%;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: rgba(15, 15, 35, 0.9);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 1rem 0;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #cbd5e1;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: #3b82f6;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            padding: 140px 0 100px;
            text-align: center;
            position: relative;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 50% 50%, rgba(59, 130, 246, 0.1) 0%, transparent 50%);
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .profile-container {
            position: relative;
            display: inline-block;
            margin-bottom: 2rem;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 4px solid rgba(59, 130, 246, 0.3);
            display: block;
            margin: 0 auto;
            transition: all 0.4s ease;
            box-shadow: 0 0 40px rgba(59, 130, 246, 0.3);
            animation: profileFloat 6s ease-in-out infinite;
        }

        @keyframes profileFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .profile-img:hover {
            transform: scale(1.05) translateY(-5px);
            box-shadow: 0 0 60px rgba(59, 130, 246, 0.5);
        }

        .profile-ring {
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border: 2px solid transparent;
            border-radius: 50%;
            background: linear-gradient(45deg, #3b82f6, #8b5cf6, #3b82f6);
            background-size: 200% 200%;
            animation: rotate 4s linear infinite;
            z-index: -1;
        }

        @keyframes rotate {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #ffffff, #cbd5e1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease-out;
            font-weight: 800;
        }

        .hero .subtitle {
            font-size: 1.4rem;
            margin-bottom: 2rem;
            color: #94a3b8;
            animation: fadeInUp 1s ease-out 0.2s both;
            font-weight: 500;
        }

        .hero .description {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            color: #cbd5e1;
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 3rem;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .social-btn {
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            padding: 1rem 2rem;
            background: rgba(59, 130, 246, 0.1);
            color: #3b82f6;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.4s ease;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(59, 130, 246, 0.3);
            position: relative;
            overflow: hidden;
        }

        .social-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .social-btn:hover::before {
            left: 100%;
        }

        .social-btn:hover {
            background: rgba(59, 130, 246, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
            color: #60a5fa;
        }

        /* Sections */
        section {
            padding: 100px 0;
            position: relative;
        }

        .section-title {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 4rem;
            background: linear-gradient(135deg, #ffffff, #cbd5e1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            font-weight: 700;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.2rem;
            color: #cbd5e1;
            line-height: 1.8;
        }

        .about-content p {
            margin-bottom: 2rem;
            padding: 2rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .about-content p:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateY(-5px);
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2.5rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
        }

        .project-card::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: -1;
        }

        .project-card:hover::after {
            opacity: 1;
        }

        .project-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 20px 40px rgba(59, 130, 246, 0.2);
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: #ffffff;
        }

        .project-description {
            color: #cbd5e1;
            line-height: 1.7;
            margin-bottom: 2rem;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-bottom: 2rem;
        }

        .tech-tag {
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.2), rgba(139, 92, 246, 0.2));
            color: #60a5fa;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-size: 0.85rem;
            font-weight: 600;
            border: 1px solid rgba(59, 130, 246, 0.3);
            transition: all 0.3s ease;
        }

        .tech-tag:hover {
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.3), rgba(139, 92, 246, 0.3));
            transform: translateY(-2px);
        }

        .project-links {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            color: #3b82f6;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 10px;
            background: rgba(59, 130, 246, 0.1);
            border: 1px solid rgba(59, 130, 246, 0.3);
        }

        .project-link:hover {
            color: #60a5fa;
            background: rgba(59, 130, 246, 0.2);
            transform: translateY(-2px);
        }

        /* Collapsible Projects */
        .projects-section {
            margin-bottom: 4rem;
        }

        .collapsible-projects {
            margin-top: 3rem;
        }

        .project-toggle {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            margin-bottom: 1rem;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .project-toggle:hover {
            background: rgba(255, 255, 255, 0.08);
        }

        .project-summary {
            padding: 1.5rem 2rem;
            cursor: pointer;
            font-weight: 600;
            color: #ffffff;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
        }

        .project-summary:hover {
            color: #3b82f6;
        }

        .project-summary::after {
            content: '+';
            font-size: 1.5rem;
            color: #3b82f6;
            transition: transform 0.3s ease;
        }

        .project-toggle[open] .project-summary::after {
            transform: rotate(45deg);
        }

        .project-details {
            padding: 0 2rem 2rem;
            color: #cbd5e1;
            line-height: 1.7;
        }

        .project-details p {
            margin-bottom: 1rem;
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.05);
            padding: 3rem 2rem;
            border-radius: 20px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .skill-category::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: -1;
        }

        .skill-category:hover::before {
            opacity: 1;
        }

        .skill-category:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
        }

        .skill-icon {
            font-size: 4rem;
            margin-bottom: 1.5rem;
            filter: drop-shadow(0 0 20px rgba(59, 130, 246, 0.5));
        }

        .skill-category h3 {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: #ffffff;
            font-weight: 700;
        }

        .skill-list {
            color: #cbd5e1;
            line-height: 2;
            font-size: 1.1rem;
        }

        /* Footer */
        footer {
            background: rgba(15, 15, 35, 0.8);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #cbd5e1;
            text-align: center;
            padding: 3rem 0;
            backdrop-filter: blur(20px);
        }

        footer a {
            color: #3b82f6;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: #60a5fa;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.8s ease-out forwards;
        }

        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .subtitle {
                font-size: 1.1rem;
            }

            .social-links {
                flex-direction: column;
                align-items: center;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .project-card {
                padding: 2rem;
            }

            .skills-container {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll animations */
        .scroll-reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease;
        }

        .scroll-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="particles" id="particles"></div>

    <header>
        <nav class="container">
            <div class="logo">Niharika MG</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-bg"></div>
        <div class="container">
            <div class="hero-content">
                <div class="profile-container">
                    <div class="profile-ring"></div>
                    <img src="https://github.com/niharikamg/portfolio/blob/main/Profile-Picture.jpg?raw=true" alt="Niharika MG" class="profile-img">
                </div>
                <h1>Hi there, I'm <span style="background: linear-gradient(135deg, #3b82f6, #8b5cf6); -webkit-background-clip: text; -webkit-text-fill-color: transparent;">Niharika MG</span></h1>
                <p class="subtitle">Cloud Engineer • Full-Stack Developer • DevOps Enthusiast</p>
                <p class="description">
                    I'm a Software Engineer passionate about building secure, scalable, and intelligent systems. I've developed cloud-native applications on AWS and Azure, built AI-powered tools, and optimized full-stack platforms using Docker and Kubernetes.
                </p>
                <div class="social-links">
                    <a href="https://www.linkedin.com/in/niharika-mg" class="social-btn" target="_blank">
                        💼 LinkedIn
                    </a>
                    <a href="mailto:mgniharikaa@gmail.com" class="social-btn" target="_blank">
                        ✉️ Email
                    </a>
                    <a href="https://niharikamg.github.io/portfolio/" class="social-btn" target="_blank">
                        🌐 Portfolio
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2 class="section-title scroll-reveal">About Me</h2>
            <div class="about-content scroll-reveal">
                <p>
                    I'm a Software Engineer passionate about building secure, scalable, and intelligent systems. I've developed cloud-native applications on AWS and Azure, built AI-powered tools, and optimized full-stack platforms using Docker and Kubernetes.
                </p>
                <p>
                    Whether it's enabling faster data insights, building secure AI models, or designing cloud services that scale — I focus on creating impactful, resilient technology. Explore my projects below!
                </p>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2 class="section-title scroll-reveal">Spotlight Projects</h2>
            <div class="projects-grid scroll-reveal">
                <div class="project-card">
                    <h3 class="project-title">CloudOps Insight – Cloud Monitoring Dashboard</h3>
                    <p class="project-description">
                        Prometheus + Grafana + Kubernetes monitoring stack with Terraform automation for comprehensive infrastructure monitoring and alerting.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">Kubernetes</span>
                        <span class="tech-tag">Prometheus</span>
                        <span class="tech-tag">Grafana</span>
                        <span class="tech-tag">Terraform</span>
                        <span class="tech-tag">GitHub Actions</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/niharikamg/CloudOps-Insight" class="project-link" target="_blank">
                            🔗 View Project
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">Azure Data Factory – ETL Pipeline</h3>
                    <p class="project-description">
                        ETL automation using ADF, Blob Storage, SQL DB and Azure Functions for real-time reporting and seamless data processing workflows.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">Azure Data Factory</span>
                        <span class="tech-tag">SQL</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Azure Functions</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/niharikamg/Azure-Data-Factory" class="project-link" target="_blank">
                            🔗 View Project
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">Decentralized AI Model Marketplace</h3>
                    <p class="project-description">
                        Blockchain-based marketplace for renting & uploading ML models using Ethereum smart contracts and IPFS for decentralized storage.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Flask</span>
                        <span class="tech-tag">Solidity</span>
                        <span class="tech-tag">Web3.js</span>
                        <span class="tech-tag">IPFS</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/niharikamg/Decentralized-AI-Model-Marketplace" class="project-link" target="_blank">
                            🔗 View Project
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">Interactive County Data Visualization</h3>
                    <p class="project-description">
                        D3.js dashboard with TopoJSON for county-level health & socioeconomic data visualization with interactive mapping features.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">JavaScript</span>
                        <span class="tech-tag">D3.js</span>
                        <span class="tech-tag">TopoJSON</span>
                        <span class="tech-tag">Data Visualization</span>
                    </div>
                    <div class="project-links">
                        <a href="https://niharikamg.github.io/Visual-Interfrace" class="project-link" target="_blank">
                            🔗 Live Demo
                        </a>
                        <a href="https://github.com/niharikamg/Visual-Interfrace" class="project-link" target="_blank">
                            📂 Repository
                        </a>
                    </div>
                </div>
            </div>

            <div class="collapsible-projects scroll-reveal">
                <h3 style="text-align: center; color: #cbd5e1; margin: 4rem 0 2rem; font-size: 2rem;">More Projects</h3>
                
                <details class="project-toggle">
                    <summary class="project-summary">AWS Flask Web App</summary>
                    <div class="project-details">
                        <p>Secure web app deployed on EC2 with authentication, upload & word count analysis.</p>
                        <p><strong>Tech Stack:</strong> Flask · EC2 · Apache · SQLite</p>
                        <a href="https://github.com/niharikamg/AWS-Flask-Web-Application-Project" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">Serverless Deployment on AWS</summary>
                    <div class="project-details">
                        <p>Built serverless event-driven services using Lambda and API Gateway with Docker.</p>
                        <p><strong>Tech Stack:</strong> AWS Lambda · Docker · GitHub Actions</p>
                        <a href="https://github.com/niharikamg/Serverless-Deployment-AWS" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">Big Data Weather Analytics</summary>
                    <div class="project-details">
                        <p>Analyzed 10+ years of weather data using PySpark with trend and extreme condition insights.</p>
                        <p><strong>Tech Stack:</strong> PySpark · Jupyter</p>
                        <a href="https://github.com/niharikamg/weather-analytics-pyspark-jupyter" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">COVID-19 Analytics with Databricks</summary>
                    <div class="project-details">
                        <p>Explored vaccination vs. mortality using PySpark and built interactive dashboards.</p>
                        <p><strong>Tech Stack:</strong> Python · Databricks · PySpark</p>
                        <a href="https://github.com/niharikamg/COVID-19-Data-Analysis-using-Databricks" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">AI Tools Suite</summary>
                    <div class="project-details">
                        <p>Includes resume analyzer, recommender, finance manager & threat detector with Flask + ML.</p>
                        <p><strong>Tech Stack:</strong> Flask · Spring Boot · ML · PostgreSQL</p>
                        <a href="https://github.com/niharikamg?tab=repositories&q=AI" class="project-link" target="_blank">🔗 View suite</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">GCP Chatbot for Student Services</summary>
                    <div class="project-details">
                        <p>Intent-based Q&A chatbot using Dialogflow, hosted via GCP App & Compute Engine.</p>
                        <p><strong>Tech Stack:</strong> Dialogflow · Python · GCP</p>
                        <a href="https://github.com/niharikamg/Google-Cloud-Platform-GCP-Chatbot-Project" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>
            </div>

            <div class="collapsible-projects scroll-reveal">
                <h3 style="text-align: center; color: #cbd5e1; margin: 4rem 0 2rem; font-size: 2rem;">🧩 Alternative Projects</h3>
                
                <details class="project-toggle">
                    <summary class="project-summary">AI-Powered Code Auto Refactoring System</summary>
                    <div class="project-details">
                        <p>Analyzes and restructures Python code for better performance using AST and ML.</p>
                        <p><strong>Tech Stack:</strong> Python · AST · NLP</p>
                        <a href="https://github.com/niharikamg/AI-Powered-Code-Auto-Refactoring-System" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">Blockchain-Based Secure Authentication System</summary>
                    <div class="project-details">
                        <p>Decentralized login/auth using Ethereum smart contracts and Web3.js — no central servers.</p>
                        <p><strong>Tech Stack:</strong> Solidity · Web3.js · Ethereum</p>
                        <a href="https://github.com/niharikamg/Blockchain-Based-Secure-Authentication-System" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">Resume Analyzer & Job Recommender</summary>
                    <div class="project-details">
                        <p>NLP-based systems for resume scoring and job matching with semantic similarity.</p>
                        <p><strong>Tech Stack:</strong> Python · Java · NLP</p>
                        <a href="https://github.com/niharikamg/AI-Based-Resume-Analyzer" class="project-link" target="_blank">Resume Analyzer</a>
                        <a href="https://github.com/niharikamg/AI-Based-Job-Recommendation-System" class="project-link" target="_blank">Job Recommender</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">AI-Powered Code Review Bot</summary>
                    <div class="project-details">
                        <p>Automated tool that reviews code for quality and optimization using machine learning.</p>
                        <p><strong>Tech Stack:</strong> Python · AI · Static Analysis</p>
                        <a href="https://github.com/niharikamg/AI-Powered-Code-Review-Bot" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">AI-Powered Financial Fraud Detection</summary>
                    <div class="project-details">
                        <p>Uses machine learning to detect suspicious financial transactions.</p>
                        <p><strong>Tech Stack:</strong> Python · ML · Fraud Detection</p>
                        <a href="https://github.com/niharikamg/AI-Powered-Financial-Fraud-Detection-System" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">Trading Bots (Classic & AI)</summary>
                    <div class="project-details">
                        <p>Cryptocurrency bots — one rule-based, one AI-enhanced — that auto-execute trades.</p>
                        <p><strong>Tech Stack:</strong> Python · ML · APIs</p>
                        <a href="https://github.com/niharikamg/Trading-Bot-Full-Project" class="project-link" target="_blank">Classic Bot</a>
                        <a href="https://github.com/niharikamg/AI-Powered-Crypto-Trading-Bot" class="project-link" target="_blank">AI Bot</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">Chatbot & Email Automation</summary>
                    <div class="project-details">
                        <p>A chatbot with NLTK and a script to send automated emails with attachments.</p>
                        <p><strong>Tech Stack:</strong> Python · NLTK · smtplib</p>
                        <a href="https://github.com/niharikamg/chatbot" class="project-link" target="_blank">Chatbot</a>
                        <a href="https://github.com/niharikamg/Automated-Email-Sender" class="project-link" target="_blank">Email Sender</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">File Utilities & CLI Tools</summary>
                    <div class="project-details">
                        <p>Includes a PDF merger, task manager, GitHub repo analyzer, and folder organizer — all terminal-based.</p>
                        <p><strong>Tech Stack:</strong> Python · Shell Scripting</p>
                        <a href="https://github.com/niharikamg/PDF-Merger-CLI" class="project-link" target="_blank">PDF Merger</a>
                        <a href="https://github.com/niharikamg/GitHub-Repo-Analyzer-CLI" class="project-link" target="_blank">Repo Analyzer</a>
                        <a href="https://github.com/niharikamg/task-manager-cli" class="project-link" target="_blank">Task Manager</a>
                        <a href="https://github.com/niharikamg/organizer" class="project-link" target="_blank">File Organizer</a>
                    </div>
                </details>

                <details class="project-toggle">
                    <summary class="project-summary">PySpark in Jupyter Notebook</summary>
                    <div class="project-details">
                        <p>Big data workflows and transformations using PySpark inside a notebook environment.</p>
                        <p><strong>Tech Stack:</strong> PySpark · Jupyter</p>
                        <a href="https://github.com/niharikamg/PySpark-in-Jupyter-Notebook" class="project-link" target="_blank">🔗 View project</a>
                    </div>
                </details>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2 class="section-title scroll-reveal">Technical Skills</h2>
            <div class="skills-container scroll-reveal">
                <div class="skill-category">
                    <div class="skill-icon">☁️</div>
                    <h3>Cloud Platforms</h3>
                    <p class="skill-list">AWS • Azure • GCP<br>Docker • Kubernetes<br>Terraform • Serverless</p>
                </div>
                <div class="skill-category">
                    <div class="skill-icon">💻</div>
                    <h3>Programming</h3>
                    <p class="skill-list">Python • JavaScript • Java<br>React • Flask • Spring Boot<br>SQL • NoSQL</p>
                </div>
                <div class="skill-category">
                    <div class="skill-icon">🤖</div>
                    <h3>AI & Machine Learning</h3>
                    <p class="skill-list">Machine Learning • NLP<br>TensorFlow • PyTorch<br>Data Analytics • PySpark</p>
                </div>
                <div class="skill-category">
                    <div class="skill-icon">🔧</div>
                    <h3>DevOps & Tools</h3>
                    <p class="skill-list">CI/CD • GitHub Actions<br>Monitoring • Grafana<br>Prometheus • Jenkins</p>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <p>&copy; 2025 Niharika MG. Built with passion for technology and innovation.</p>
            <p style="margin-top: 1rem; opacity: 0.8;">
                <a href="mailto:mgniharikaa@gmail.com">mgniharikaa@gmail.com</a> • 
                <a href="https://www.linkedin.com/in/niharika-mg" target="_blank">LinkedIn</a> •
                <a href="https://niharikamg.github.io/portfolio/" target="_blank">Portfolio</a>
            </p>
        </div>
    </footer>

    <script>
        // Create animated background particles
        function createParticles() {
            const particles = document.getElementById('particles');
            const particleCount = 50;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                const size = Math.random() * 4 + 2;
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 3) + 's';
                
                particles.appendChild(particle);
            }
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Scroll reveal animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('revealed');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.scroll-reveal').forEach(element => {
            observer.observe(element);
        });

        // Header background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(15, 15, 35, 0.95)';
            } else {
                header.style.background = 'rgba(15, 15, 35, 0.9)';
            }
        });

        // Initialize
        createParticles();
    </script>
</body>
</html>
