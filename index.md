<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Niharika MG | Next-Gen Cloud Engineer & AI Developer</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;600;700;800&family=Inter:wght@300;400;500;600;700;800;900&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            /* Space-inspired color palette */
            --primary-bg: #0B0C10;
            --secondary-bg: #1F2833;
            --tertiary-bg: #2A2D3A;
            --accent-cosmic: #66FCF1;
            --accent-nebula: #45A29E;
            --accent-starlight: #C5C6C7;
            --accent-purple: #8B7ED8;
            --accent-deep-purple: #5D4E75;
            --text-primary: #FFFFFF;
            --text-secondary: #C5C6C7;
            --text-muted: #8892B0;
            --glass-bg: rgba(197, 198, 199, 0.03);
            --glass-border: rgba(102, 252, 241, 0.2);
            --glow-cosmic: 0 0 30px rgba(102, 252, 241, 0.4);
            --glow-nebula: 0 0 30px rgba(69, 162, 158, 0.4);
            --glow-starlight: 0 0 30px rgba(197, 198, 199, 0.3);
            --glow-purple: 0 0 30px rgba(139, 126, 216, 0.4);
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, var(--primary-bg) 0%, var(--secondary-bg) 50%, var(--tertiary-bg) 100%);
            color: var(--text-primary);
            overflow-x: hidden;
            line-height: 1.6;
            position: relative;
        }

        /* Cosmic Background Grid */
        .tech-grid {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(102, 252, 241, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(102, 252, 241, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -3;
            animation: grid-pulse 4s ease-in-out infinite;
        }

        @keyframes grid-pulse {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        /* Cosmic Particles */
        .cyber-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -2;
            overflow: hidden;
        }

        .cyber-particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: var(--accent-cosmic);
            border-radius: 50%;
            box-shadow: var(--glow-cosmic);
            animation: cosmic-float 8s linear infinite;
        }

        @keyframes cosmic-float {
            0% {
                transform: translateY(100vh) translateX(0);
                opacity: 0;
            }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% {
                transform: translateY(-100px) translateX(100px);
                opacity: 0;
            }
        }

        /* Galactic Orbs */
        .holo-orbs {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .holo-orb {
            position: absolute;
            border-radius: 50%;
            background: conic-gradient(from 0deg, var(--accent-cosmic), var(--accent-nebula), var(--accent-purple), var(--accent-cosmic));
            filter: blur(60px);
            opacity: 0.15;
            animation: galactic-drift 20s ease-in-out infinite;
        }

        .holo-orb:nth-child(1) {
            width: 400px;
            height: 400px;
            top: 20%;
            left: 10%;
            animation-delay: -5s;
        }

        .holo-orb:nth-child(2) {
            width: 300px;
            height: 300px;
            top: 60%;
            right: 15%;
            animation-delay: -12s;
        }

        .holo-orb:nth-child(3) {
            width: 500px;
            height: 500px;
            bottom: 15%;
            left: 40%;
            animation-delay: -8s;
        }

        @keyframes galactic-drift {
            0%, 100% { transform: translate(0, 0) scale(1); }
            25% { transform: translate(50px, -100px) scale(1.1); }
            50% { transform: translate(-30px, 80px) scale(0.9); }
            75% { transform: translate(70px, 40px) scale(1.05); }
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Mobile Navigation Toggle */
        .nav-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            padding: 0.5rem;
        }

        .nav-toggle span {
            width: 25px;
            height: 3px;
            background: var(--accent-cosmic);
            margin: 2px 0;
            transition: 0.3s;
            border-radius: 2px;
        }

        .nav-toggle.active span:nth-child(1) {
            transform: rotate(45deg) translate(5px, 5px);
        }

        .nav-toggle.active span:nth-child(2) {
            opacity: 0;
        }

        .nav-toggle.active span:nth-child(3) {
            transform: rotate(-45deg) translate(7px, -6px);
        }

        /* Space Header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 1.5rem 0;
            background: rgba(11, 12, 16, 0.8);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid var(--glass-border);
            transition: all 0.3s ease;
        }

        .header-active {
            background: rgba(11, 12, 16, 0.95);
            box-shadow: var(--glow-cosmic);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'JetBrains Mono', monospace;
            font-size: 1.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--accent-cosmic), var(--accent-starlight));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .logo::before {
            content: '> ';
            color: var(--accent-nebula);
            animation: cursor-blink 1s infinite;
        }

        @keyframes cursor-blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        .nav-links a {
            font-family: 'JetBrains Mono', monospace;
            text-decoration: none;
            color: var(--text-secondary);
            font-weight: 500;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            position: relative;
            padding: 0.5rem 1rem;
            border-radius: 8px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-links a::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--glass-bg), transparent);
            border: 1px solid transparent;
            border-radius: 8px;
            opacity: 0;
            transition: all 0.3s ease;
            z-index: -1;
        }

        .nav-links a:hover::before {
            opacity: 1;
            border-color: var(--accent-cosmic);
            box-shadow: var(--glow-cosmic);
        }

        .nav-links a:hover {
            color: var(--accent-cosmic);
            transform: translateY(-2px);
        }

        /* Revolutionary Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            padding: 120px 0;
        }

        .hero-bg-effect {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 50% 50%, rgba(102, 252, 241, 0.1) 0%, transparent 70%);
            z-index: -1;
        }

        .hero-content {
            z-index: 1;
        }

        .profile-tech-frame {
            position: relative;
            margin-bottom: 3rem;
            display: inline-block;
        }

        .profile-holo-ring {
            position: absolute;
            top: -20px;
            left: -20px;
            right: -20px;
            bottom: -20px;
            border: 2px solid transparent;
            border-radius: 50%;
            background: conic-gradient(from 0deg, var(--accent-cosmic), var(--accent-nebula), var(--accent-purple), var(--accent-cosmic)) border-box;
            mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0);
            mask-composite: exclude;
            animation: galactic-rotate 8s linear infinite;
        }

        @keyframes galactic-rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 3px solid var(--accent-cosmic);
            display: block;
            transition: all 0.5s ease;
            box-shadow: 
                var(--glow-cosmic),
                0 0 60px rgba(102, 252, 241, 0.2),
                inset 0 0 30px rgba(255, 255, 255, 0.1);
            animation: profile-pulse 4s ease-in-out infinite;
        }

        @keyframes profile-pulse {
            0%, 100% {
                box-shadow: 
                    var(--glow-cosmic),
                    0 0 60px rgba(102, 252, 241, 0.2),
                    inset 0 0 30px rgba(255, 255, 255, 0.1);
            }
            50% {
                box-shadow: 
                    0 0 50px rgba(102, 252, 241, 0.6),
                    0 0 100px rgba(102, 252, 241, 0.3),
                    inset 0 0 50px rgba(255, 255, 255, 0.2);
            }
        }

        .profile-img:hover {
            transform: scale(1.05);
            box-shadow: 
                0 0 80px rgba(102, 252, 241, 0.8),
                0 0 160px rgba(102, 252, 241, 0.4);
        }

        .tech-badge {
            position: absolute;
            top: -10px;
            right: -10px;
            background: linear-gradient(135deg, var(--accent-nebula), var(--accent-purple));
            color: white;
            padding: 0.5rem;
            border-radius: 50%;
            font-size: 1.2rem;
            animation: badge-float 3s ease-in-out infinite;
        }

        @keyframes badge-float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .hero h1 {
            font-family: 'JetBrains Mono', monospace;
            font-size: clamp(2rem, 8vw, 5rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, 
                var(--text-primary) 0%, 
                var(--accent-cosmic) 30%, 
                var(--accent-nebula) 60%, 
                var(--accent-starlight) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: text-hologram 3s ease-in-out infinite;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        @keyframes text-hologram {
            0%, 100% { 
                background-position: 0% 50%;
                filter: hue-rotate(0deg);
            }
            50% { 
                background-position: 100% 50%;
                filter: hue-rotate(180deg);
            }
        }

        .hero .subtitle {
            font-family: 'JetBrains Mono', monospace;
            font-size: clamp(1rem, 3vw, 1.2rem);
            font-weight: 600;
            margin-bottom: 2rem;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 2px;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .hero .description {
            font-size: clamp(1rem, 2.5vw, 1.1rem);
            max-width: 700px;
            margin: 0 auto 3rem;
            color: var(--text-secondary);
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        /* Space Social Links */
        .social-tech {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 3rem;
            animation: fadeInUp 1s ease-out 0.9s both;
            flex-wrap: wrap;
        }

        .social-tech-btn {
            position: relative;
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            padding: 1rem 2rem;
            background: var(--glass-bg);
            color: var(--accent-cosmic);
            text-decoration: none;
            border-radius: 12px;
            font-family: 'JetBrains Mono', monospace;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.4s ease;
            backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            overflow: hidden;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .social-tech-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, 
                transparent, 
                rgba(102, 252, 241, 0.2), 
                transparent);
            transition: left 0.5s ease;
        }

        .social-tech-btn:hover::before {
            left: 100%;
        }

        .social-tech-btn:hover {
            transform: translateY(-3px);
            box-shadow: var(--glow-cosmic);
            border-color: var(--accent-cosmic);
            color: var(--text-primary);
        }

        /* Advanced Sections */
        section {
            padding: 100px 0;
            position: relative;
        }

        .section-tech-title {
            font-family: 'JetBrains Mono', monospace;
            text-align: center;
            font-size: clamp(2rem, 6vw, 3.5rem);
            font-weight: 800;
            margin-bottom: 4rem;
            background: linear-gradient(135deg, 
                var(--text-primary) 0%, 
                var(--accent-cosmic) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        .section-tech-title::before {
            content: '[';
            color: var(--accent-nebula);
            margin-right: 1rem;
        }

        .section-tech-title::after {
            content: ']';
            color: var(--accent-nebula);
            margin-left: 1rem;
        }

        /* Cosmic About Section */
        .about-tech {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .about-tech-card {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 4rem;
            backdrop-filter: blur(30px);
            box-shadow: 
                0 20px 40px rgba(0, 0, 0, 0.2),
                var(--glow-cosmic);
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
        }

        .about-tech-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, 
                transparent, 
                rgba(102, 252, 241, 0.05), 
                transparent);
            animation: card-scan 10s linear infinite;
            z-index: -1;
        }

        @keyframes card-scan {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .about-tech-card:hover {
            transform: translateY(-10px);
            box-shadow: 
                0 30px 60px rgba(0, 0, 0, 0.3),
                0 0 80px rgba(102, 252, 241, 0.3);
        }

        .about-tech-text {
            font-size: clamp(1rem, 2.5vw, 1.2rem);
            line-height: 1.8;
            color: var(--text-secondary);
            margin-bottom: 2rem;
        }

        /* Revolutionary Project Grid */
        .projects-tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2.5rem;
            margin-top: 4rem;
        }

        .project-tech-card {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 16px;
            padding: 2.5rem;
            backdrop-filter: blur(30px);
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .project-tech-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, 
                var(--accent-cosmic), 
                var(--accent-nebula), 
                var(--accent-purple));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }

        .project-tech-card:hover::before {
            transform: scaleX(1);
        }

        .project-tech-card::after {
            content: '';
            position: absolute;
            top: -100%;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, 
                transparent, 
                rgba(102, 252, 241, 0.05), 
                transparent);
            transition: top 0.5s ease;
        }

        .project-tech-card:hover::after {
            top: 100%;
        }

        .project-tech-card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 
                0 25px 50px rgba(102, 252, 241, 0.2),
                var(--glow-cosmic);
            border-color: var(--accent-cosmic);
        }

        .project-tech-title {
            font-family: 'JetBrains Mono', monospace;
            font-size: clamp(1.1rem, 2.5vw, 1.3rem);
            font-weight: 700;
            margin-bottom: 1.5rem;
            color: var(--text-primary);
            background: linear-gradient(135deg, 
                var(--text-primary), 
                var(--accent-cosmic));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .project-tech-description {
            color: var(--text-secondary);
            line-height: 1.7;
            margin-bottom: 2rem;
            font-size: clamp(0.9rem, 2vw, 1rem);
        }

        .project-tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-bottom: 2rem;
        }

        .tech-stack-tag {
            background: linear-gradient(135deg, 
                rgba(102, 252, 241, 0.1), 
                rgba(69, 162, 158, 0.1));
            color: var(--accent-cosmic);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-family: 'JetBrains Mono', monospace;
            font-size: clamp(0.7rem, 1.5vw, 0.8rem);
            font-weight: 600;
            border: 1px solid var(--glass-border);
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .tech-stack-tag:hover {
            background: linear-gradient(135deg, 
                var(--accent-cosmic), 
                var(--accent-nebula));
            color: var(--primary-bg);
            transform: translateY(-2px) scale(1.05);
            box-shadow: var(--glow-cosmic);
        }

        .project-tech-links {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .project-tech-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--accent-cosmic);
            text-decoration: none;
            font-family: 'JetBrains Mono', monospace;
            font-weight: 600;
            font-size: clamp(0.8rem, 1.8vw, 0.9rem);
            transition: all 0.3s ease;
            padding: 0.8rem 1.5rem;
            border-radius: 10px;
            background: rgba(102, 252, 241, 0.1);
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(10px);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .project-tech-link:hover {
            background: var(--accent-cosmic);
            color: var(--primary-bg);
            transform: translateY(-2px);
            box-shadow: var(--glow-cosmic);
            border-color: var(--accent-cosmic);
        }

        /* Advanced Collapsible Projects */
        .projects-tech-collapsible {
            margin-top: 5rem;
        }

        .section-tech-subtitle {
            font-family: 'JetBrains Mono', monospace;
            text-align: center;
            color: var(--text-secondary);
            margin: 5rem 0 3rem;
            font-size: clamp(1.5rem, 4vw, 2rem);
            font-weight: 700;
            background: linear-gradient(135deg, 
                var(--text-secondary), 
                var(--accent-cosmic));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .project-tech-toggle {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            border-radius: 12px;
            margin-bottom: 1.5rem;
            overflow: hidden;
            backdrop-filter: blur(30px);
            transition: all 0.3s ease;
        }

        .project-tech-toggle:hover {
            background: rgba(102, 252, 241, 0.05);
            box-shadow: var(--glow-cosmic);
            border-color: var(--accent-cosmic);
        }

        .project-tech-summary {
            padding: 1.5rem 2rem;
            cursor: pointer;
            font-family: 'JetBrains Mono', monospace;
            font-weight: 700;
            font-size: clamp(1rem, 2.5vw, 1.1rem);
            color: var(--text-primary);
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
            position: relative;
        }

        .project-tech-summary::before {
            content: '>';
            color: var(--accent-cosmic);
            margin-right: 1rem;
            transition: transform 0.3s ease;
        }

        .project-tech-toggle[open] .project-tech-summary::before {
            transform: rotate(90deg);
        }

        .project-tech-summary:hover {
            color: var(--accent-cosmic);
        }

        .project-tech-summary::after {
            content: '[+]';
            font-size: clamp(0.9rem, 2vw, 1rem);
            color: var(--accent-nebula);
            transition: all 0.3s ease;
        }

        .project-tech-toggle[open] .project-tech-summary::after {
            content: '[-]';
            color: var(--accent-starlight);
        }

        .project-tech-details {
            padding: 0 2rem 2rem;
            color: var(--text-secondary);
            line-height: 1.7;
            font-size: clamp(0.9rem, 2vw, 1rem);
            border-top: 1px solid var(--glass-border);
        }

        /* Cosmic Skills Section */
        .skills-tech-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            margin-top: 4rem;
        }

        .skill-tech-category {
            background: var(--glass-bg);
            padding: 3rem 2rem;
            border-radius: 16px;
            text-align: center;
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(30px);
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
        }

        .skill-tech-category::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, 
                transparent, 
                rgba(102, 252, 241, 0.05), 
                transparent);
            animation: skill-scan 15s linear infinite;
            z-index: -1;
        }

        @keyframes skill-scan {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .skill-tech-category:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: var(--glow-cosmic);
            border-color: var(--accent-cosmic);
        }

        .skill-tech-icon {
            font-size: clamp(3rem, 6vw, 4rem);
            margin-bottom: 2rem;
            filter: drop-shadow(var(--glow-cosmic));
            animation: icon-tech-float 4s ease-in-out infinite;
        }

        @keyframes icon-tech-float {
            0%, 100% { 
                transform: translateY(0px);
                filter: drop-shadow(var(--glow-cosmic));
            }
            50% { 
                transform: translateY(-10px);
                filter: drop-shadow(0 0 40px var(--accent-cosmic));
            }
        }

        .skill-tech-category h3 {
            font-family: 'JetBrains Mono', monospace;
            font-size: clamp(1.1rem, 2.5vw, 1.3rem);
            margin-bottom: 2rem;
            color: var(--text-primary);
            font-weight: 700;
            background: linear-gradient(135deg, 
                var(--text-primary), 
                var(--accent-cosmic));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .skill-tech-list {
            color: var(--text-secondary);
            line-height: 2;
            font-size: clamp(0.9rem, 2vw, 1rem);
        }

        /* Space Footer */
        footer {
            background: linear-gradient(135deg, 
                rgba(11, 12, 16, 0.95), 
                rgba(31, 40, 51, 0.95));
            border-top: 2px solid var(--accent-cosmic);
            color: var(--text-secondary);
            text-align: center;
            padding: 3rem 0;
            backdrop-filter: blur(30px);
            position: relative;
        }

        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, 
                transparent, 
                var(--accent-cosmic), 
                var(--accent-nebula), 
                var(--accent-starlight), 
                transparent);
            animation: footer-scan 3s ease-in-out infinite;
        }

        @keyframes footer-scan {
            0%, 100% { opacity: 0.7; }
            50% { opacity: 1; }
        }

        footer a {
            color: var(--accent-cosmic);
            text-decoration: none;
            font-family: 'JetBrains Mono', monospace;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        footer a:hover {
            color: var(--accent-starlight);
            text-shadow: var(--glow-starlight);
        }

        footer p {
            font-size: clamp(0.9rem, 2vw, 1rem);
            margin-bottom: 1rem;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .scroll-tech-reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease;
        }

        .scroll-tech-reveal.revealed {
            opacity: 1;
            transform: translateY(0);
        }

        /* Enhanced Mobile Responsiveness */
        @media (max-width: 1024px) {
            .projects-tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
                gap: 2rem;
            }
            
            .skills-tech-container {
                grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
                gap: 2rem;
            }

            .container {
                padding: 0 1.5rem;
            }
        }

        @media (max-width: 768px) {
            .nav-toggle {
                display: flex;
            }

            .nav-links {
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: rgba(11, 12, 16, 0.95);
                backdrop-filter: blur(20px);
                flex-direction: column;
                gap: 0;
                transform: translateY(-100%);
                opacity: 0;
                visibility: hidden;
                transition: all 0.3s ease;
                border-top: 1px solid var(--glass-border);
            }

            .nav-links.active {
                transform: translateY(0);
                opacity: 1;
                visibility: visible;
            }

            .nav-links li {
                border-bottom: 1px solid var(--glass-border);
            }

            .nav-links li:last-child {
                border-bottom: none;
            }

            .nav-links a {
                display: block;
                padding: 1rem 2rem;
                font-size: 1rem;
            }

            .container {
                padding: 0 1rem;
            }

            .hero {
                padding: 100px 0 80px;
                min-height: 90vh;
            }

            .profile-img {
                width: 150px;
                height: 150px;
            }

            .social-tech {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
                max-width: 300px;
                margin: 3rem auto 0;
            }

            .social-tech-btn {
                width: 100%;
                justify-content: center;
                padding: 1rem;
            }

            .project-tech-card,
            .skill-tech-category {
                padding: 2rem 1.5rem;
            }

            .about-tech-card {
                padding: 2.5rem 1.5rem;
            }

            .project-tech-summary {
                padding: 1.5rem;
                font-size: 1rem;
                flex-wrap: wrap;
                text-align: left;
            }

            .project-tech-details {
                padding: 0 1.5rem 2rem;
            }

            .projects-tech-grid {
                grid-template-columns: 1fr;
                gap: 1.5rem;
            }

            .skills-tech-container {
                grid-template-columns: 1fr;
                gap: 1.5rem;
            }

            section {
                padding: 80px 0;
            }

            .tech-stack-tag {
                font-size: 0.7rem;
                padding: 0.4rem 0.8rem;
            }

            .project-tech-links {
                flex-direction: column;
                gap: 0.8rem;
            }

            .project-tech-link {
                text-align: center;
                justify-content: center;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
                letter-spacing: 1px;
            }

            .hero .subtitle {
                font-size: 0.9rem;
                letter-spacing: 1px;
            }

            .section-tech-title {
                font-size: 2rem;
                letter-spacing: 1px;
            }

            .project-tech-card,
            .skill-tech-category,
            .about-tech-card {
                padding: 1.5rem 1rem;
            }

            .profile-img {
                width: 120px;
                height: 120px;
            }

            .logo {
                font-size: 1.2rem;
            }
        }

        /* Cosmic Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: var(--secondary-bg);
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(180deg, 
                var(--accent-cosmic), 
                var(--accent-nebula));
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(180deg, 
                var(--accent-nebula), 
                var(--accent-starlight));
        }

        /* Loading Screen */
        .tech-loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--primary-bg);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }

        .tech-loader.hidden {
            opacity: 0;
            pointer-events: none;
        }

        .loader-tech-ring {
            width: 100px;
            height: 100px;
            border: 3px solid transparent;
            border-top: 3px solid var(--accent-cosmic);
            border-radius: 50%;
            animation: cosmic-spin 1s linear infinite;
            box-shadow: var(--glow-cosmic);
        }

        @keyframes cosmic-spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Enhanced Mobile Menu Animation */
        @media (max-width: 768px) {
            .nav-links a:hover {
                background: rgba(102, 252, 241, 0.1);
                transform: translateX(10px);
            }
        }
    </style>
</head>
<body>
    <!-- Space Loading Screen -->
    <div class="tech-loader" id="loader">
        <div class="loader-tech-ring"></div>
    </div>

    <!-- Cosmic Background Effects -->
    <div class="tech-grid"></div>
    <div class="cyber-particles" id="cyberParticles"></div>
    <div class="holo-orbs">
        <div class="holo-orb"></div>
        <div class="holo-orb"></div>
        <div class="holo-orb"></div>
    </div>

    <header id="header">
        <nav class="container">
            <div class="logo">Niharika.MG</div>
            <div class="nav-toggle" id="navToggle">
                <span></span>
                <span></span>
                <span></span>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-bg-effect"></div>
        <div class="container">
            <div class="hero-content">
                <div class="profile-tech-frame">
                    <div class="profile-holo-ring"></div>
                    <img src="https://github.com/niharikamg/portfolio/blob/main/Profile-Picture.jpg?raw=true" alt="Niharika MG" class="profile-img">
                    <div class="tech-badge">⚡</div>
                </div>
                <h1>Niharika MG</h1>
                <p class="subtitle">Next-Gen Cloud Engineer • AI Developer • DevOps Architect</p>
                <p class="description">
                    Engineering the future with cutting-edge cloud-native solutions, revolutionary AI systems, and enterprise-scale infrastructure. Specializing in AWS/Azure architectures, advanced machine learning, and next-generation DevOps automation.
                </p>
                <div class="social-tech">
                    <a href="https://www.linkedin.com/in/niharika-mg" class="social-tech-btn" target="_blank">
                        🔗 LinkedIn
                    </a>
                    <a href="mailto:mgniharikaa@gmail.com" class="social-tech-btn" target="_blank">
                        📧 Contact
                    </a>
                    <a href="https://niharikamg.github.io/portfolio/" class="social-tech-btn" target="_blank">
                        🌐 Portfolio
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2 class="section-tech-title scroll-tech-reveal">About</h2>
            <div class="about-tech scroll-tech-reveal">
                <div class="about-tech-card">
                    <p class="about-tech-text">
                        Next-generation Software Engineer specializing in architecting secure, scalable, and intelligent systems that push the boundaries of what's possible. Expert in cloud-native development across AWS and Azure, with deep expertise in AI/ML solutions and enterprise DevOps automation.
                    </p>
                    <p class="about-tech-text">
                        From real-time data processing pipelines to blockchain-based decentralized applications, I build technology that scales infinitely and delivers transformational business impact. Experience the future of software engineering.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2 class="section-tech-title scroll-tech-reveal">Projects</h2>
            <div class="projects-tech-grid scroll-tech-reveal">
                <div class="project-tech-card">
                    <h3 class="project-tech-title">CloudOps Insight Dashboard (Ongoing) </h3>
                    <p class="project-tech-description">
                        Next-gen monitoring platform combining Prometheus, Grafana, and Kubernetes with automated Terraform deployment. Features real-time alerting, predictive analytics, and intelligent resource optimization.
                    </p>
                    <div class="project-tech-stack">
                        <span class="tech-stack-tag">Kubernetes</span>
                        <span class="tech-stack-tag">Prometheus</span>
                        <span class="tech-stack-tag">Grafana</span>
                        <span class="tech-stack-tag">Terraform</span>
                        <span class="tech-stack-tag">CI/CD</span>
                    </div>
                    <div class="project-tech-links">
                        <a href="https://github.com/niharikamg/CloudOps-Insight-Cloud-Monitoring-Deployment-Dashboard" class="project-tech-link" target="_blank">
                            View Code
                        </a>
                    </div>
                </div>

                <div class="project-tech-card">
                    <h3 class="project-tech-title">Azure ETL Pipeline</h3>
                    <p class="project-tech-description">
                        Advanced data processing pipeline using Azure Data Factory with real-time streaming, automated scaling, and intelligent error handling. Processes millions of records with zero downtime.
                    </p>
                    <div class="project-tech-stack">
                        <span class="tech-stack-tag">Azure DF</span>
                        <span class="tech-stack-tag">SQL</span>
                        <span class="tech-stack-tag">Python</span>
                        <span class="tech-stack-tag">Functions</span>
                    </div>
                    <div class="project-tech-links">
                        <a href="https://github.com/niharikamg/Azure-Data-Factory" class="project-tech-link" target="_blank">
                            View Code
                        </a>
                    </div>
                </div>

                <div class="project-tech-card">
                    <h3 class="project-tech-title">AI Tools Suite</h3>
                    <p class="project-tech-description">
                        Comprehensive AI toolkit including resume analysis, job recommendations, financial management, and threat detection with advanced ML algorithms. Features intelligent automation and data processing.
                    </p>
                    <div class="project-tech-stack">
                        <span class="tech-stack-tag">Flask</span>
                        <span class="tech-stack-tag">Spring Boot</span>
                        <span class="tech-stack-tag">ML</span>
                        <span class="tech-stack-tag">PostgreSQL</span>
                    </div>
                    <div class="project-tech-links">
                        <a href="https://github.com/niharikamg?tab=repositories&q=AI" class="project-tech-link" target="_blank">
                            View Suite
                        </a>
                    </div>
                </div>

                <div class="project-tech-card">
                    <h3 class="project-tech-title">Interactive Data Visualization</h3>
                    <p class="project-tech-description">
                        Advanced D3.js dashboard with TopoJSON integration for real-time county-level data visualization. Features interactive mapping, dynamic filtering, and responsive design.
                    </p>
                    <div class="project-tech-stack">
                        <span class="tech-stack-tag">D3.js</span>
                        <span class="tech-stack-tag">TopoJSON</span>
                        <span class="tech-stack-tag">JavaScript</span>
                        <span class="tech-stack-tag">SVG</span>
                    </div>
                    <div class="project-tech-links">
                        <a href="https://niharikamg.github.io/Visual-Interfrace" class="project-tech-link" target="_blank">
                            Live Demo
                        </a>
                        <a href="https://github.com/niharikamg/Visual-Interfrace" class="project-tech-link" target="_blank">
                            View Code
                        </a>
                    </div>
                </div>
            </div>

            <div class="projects-tech-collapsible scroll-tech-reveal">
                <h3 class="section-tech-subtitle">Additional Projects</h3>
                
                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">AWS Flask Application</summary>
                    <div class="project-tech-details">
                        <p>Enterprise-grade web application with advanced authentication, file processing, and analytics. Deployed on EC2 with auto-scaling and load balancing.</p>
                        <p><strong>Tech Stack:</strong> Flask • EC2 • Apache • SQLite • AWS</p>
                        <a href="https://github.com/niharikamg/AWS-Flask-Web-Application-Project" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Serverless Architecture</summary>
                    <div class="project-tech-details">
                        <p>Event-driven microservices using AWS Lambda, API Gateway, and Docker. Features automatic scaling, cost optimization, and zero-downtime deployments.</p>
                        <p><strong>Tech Stack:</strong> Lambda • Docker • API Gateway • CI/CD</p>
                        <a href="https://github.com/niharikamg/Serverless-Deployment-AWS" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Big Data Weather Analytics</summary>
                    <div class="project-tech-details">
                        <p>Large-scale weather data analysis using PySpark with machine learning for pattern recognition and climate prediction modeling.</p>
                        <p><strong>Tech Stack:</strong> PySpark • Jupyter • ML • Big Data</p>
                        <a href="https://github.com/niharikamg/weather-analytics-pyspark-jupyter" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">COVID-19 Analytics Platform</summary>
                    <div class="project-tech-details">
                        <p>Comprehensive data analysis platform using Databricks for vaccination tracking, mortality analysis, and interactive reporting dashboards.</p>
                        <p><strong>Tech Stack:</strong> Databricks • PySpark • Python • Analytics</p>
                        <a href="https://github.com/niharikamg/COVID-19-Data-Analysis-using-Databricks" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Decentralized AI Marketplace</summary>
                    <div class="project-tech-details">
                        <p>Revolutionary blockchain-based platform for AI model trading using Ethereum smart contracts, IPFS storage, and Web3 integration. Enables secure, decentralized AI commerce.</p>
                        <p><strong>Tech Stack:</strong> React • Solidity • Web3 • IPFS</p>
                        <a href="https://github.com/niharikamg/Decentralized-AI-Model-Marketplace" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">GCP Intelligent Chatbot</summary>
                    <div class="project-tech-details">
                        <p>Advanced conversational AI using Dialogflow with natural language understanding, context awareness, and multi-platform deployment.</p>
                        <p><strong>Tech Stack:</strong> Dialogflow • Python • GCP • NLP</p>
                        <a href="https://github.com/niharikamg/Google-Cloud-Platform-GCP-Chatbot-Project" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>
            </div>

            <div class="projects-tech-collapsible scroll-tech-reveal">
                <h3 class="section-tech-subtitle">Specialized Solutions</h3>
                
                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">AI Code Refactoring Engine</summary>
                    <div class="project-tech-details">
                        <p>Intelligent code optimization system using AST analysis and machine learning to automatically improve code performance, readability, and maintainability.</p>
                        <p><strong>Tech Stack:</strong> Python • AST • ML • NLP</p>
                        <a href="https://github.com/niharikamg/AI-Powered-Code-Auto-Refactoring-System" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Blockchain Authentication</summary>
                    <div class="project-tech-details">
                        <p>Decentralized authentication system eliminating traditional servers using Ethereum smart contracts and cryptographic verification.</p>
                        <p><strong>Tech Stack:</strong> Solidity • Web3.js • Ethereum • Crypto</p>
                        <a href="https://github.com/niharikamg/Blockchain-Based-Secure-Authentication-System" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">AI Resume & Job Matching</summary>
                    <div class="project-tech-details">
                        <p>Advanced NLP system for intelligent resume analysis and job matching using semantic similarity, skill extraction, and recommendation algorithms.</p>
                        <p><strong>Tech Stack:</strong> Python • Java • NLP • ML</p>
                        <a href="https://github.com/niharikamg/AI-Based-Resume-Analyzer" class="project-tech-link" target="_blank">Resume Analyzer</a>
                        <a href="https://github.com/niharikamg/AI-Based-Job-Recommendation-System" class="project-tech-link" target="_blank">Job Recommender</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Intelligent Code Review Bot</summary>
                    <div class="project-tech-details">
                        <p>Automated code quality assessment using machine learning for bug detection, security analysis, and performance optimization recommendations.</p>
                        <p><strong>Tech Stack:</strong> Python • AI • Static Analysis • ML</p>
                        <a href="https://github.com/niharikamg/AI-Powered-Code-Review-Bot" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Financial Fraud Detection AI</summary>
                    <div class="project-tech-details">
                        <p>Real-time fraud detection system using advanced machine learning algorithms for anomaly detection and risk assessment in financial transactions.</p>
                        <p><strong>Tech Stack:</strong> Python • ML • Fraud Detection • Real-time</p>
                        <a href="https://github.com/niharikamg/AI-Powered-Financial-Fraud-Detection-System" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Crypto Trading AI Suite</summary>
                    <div class="project-tech-details">
                        <p>Sophisticated algorithmic trading systems with both rule-based and AI-enhanced strategies for automated cryptocurrency trading and portfolio management.</p>
                        <p><strong>Tech Stack:</strong> Python • ML • APIs • Algorithms</p>
                        <a href="https://github.com/niharikamg/Trading-Bot-Full-Project" class="project-tech-link" target="_blank">Classic Bot</a>
                        <a href="https://github.com/niharikamg/AI-Powered-Crypto-Trading-Bot" class="project-tech-link" target="_blank">AI Bot</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Intelligent Automation Suite</summary>
                    <div class="project-tech-details">
                        <p>Advanced chatbot with NLP capabilities and automated email system with smart attachment handling and scheduling features.</p>
                        <p><strong>Tech Stack:</strong> Python • NLTK • NLP • Automation</p>
                        <a href="https://github.com/niharikamg/chatbot" class="project-tech-link" target="_blank">Chatbot</a>
                        <a href="https://github.com/niharikamg/Automated-Email-Sender" class="project-tech-link" target="_blank">Email System</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Developer Tools Suite</summary>
                    <div class="project-tech-details">
                        <p>Professional command-line utilities including PDF processing, task management, repository analysis, and file organization with automation features.</p>
                        <p><strong>Tech Stack:</strong> Python • CLI • Shell Scripting • Automation</p>
                        <a href="https://github.com/niharikamg/PDF-Merger-CLI" class="project-tech-link" target="_blank">PDF Tools</a>
                        <a href="https://github.com/niharikamg/GitHub-Repo-Analyzer-CLI" class="project-tech-link" target="_blank">Repo Analyzer</a>
                        <a href="https://github.com/niharikamg/task-manager-cli" class="project-tech-link" target="_blank">Task Manager</a>
                        <a href="https://github.com/niharikamg/organizer" class="project-tech-link" target="_blank">File Organizer</a>
                    </div>
                </details>

                <details class="project-tech-toggle">
                    <summary class="project-tech-summary">Big Data Processing Platform</summary>
                    <div class="project-tech-details">
                        <p>Comprehensive big data processing environment using PySpark in Jupyter with advanced analytics, visualization, and distributed computing capabilities.</p>
                        <p><strong>Tech Stack:</strong> PySpark • Jupyter • Big Data • Analytics</p>
                        <a href="https://github.com/niharikamg/PySpark-in-Jupyter-Notebook" class="project-tech-link" target="_blank">View Code</a>
                    </div>
                </details>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2 class="section-tech-title scroll-tech-reveal">Skills</h2>
            <div class="skills-tech-container scroll-tech-reveal">
                <div class="skill-tech-category">
                    <div class="skill-tech-icon">☁️</div>
                    <h3>Cloud Architecture</h3>
                    <p class="skill-tech-list">AWS • Azure • Google Cloud<br>Kubernetes • Docker<br>Terraform • Serverless</p>
                </div>
                <div class="skill-tech-category">
                    <div class="skill-tech-icon">⚡</div>
                    <h3>Development</h3>
                    <p class="skill-tech-list">Python • JavaScript • Java<br>React • Flask • Spring Boot<br>APIs • Microservices</p>
                </div>
                <div class="skill-tech-category">
                    <div class="skill-tech-icon">🤖</div>
                    <h3>AI & Machine Learning</h3>
                    <p class="skill-tech-list">Machine Learning • Deep Learning<br>NLP • Computer Vision<br>TensorFlow • PyTorch</p>
                </div>
                <div class="skill-tech-category">
                    <div class="skill-tech-icon">🔧</div>
                    <h3>DevOps & Automation</h3>
                    <p class="skill-tech-list">CI/CD • GitHub Actions<br>Monitoring • Grafana<br>Jenkins • Automation</p>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <p>&copy; 2025 Niharika MG. Engineered with cutting-edge technology and innovation.</p>
            <p style="margin-top: 1.5rem;">
                <a href="mailto:mgniharikaa@gmail.com">Contact</a> • 
                <a href="https://www.linkedin.com/in/niharika-mg" target="_blank">LinkedIn</a> •
                <a href="https://niharikamg.github.io/portfolio/" target="_blank">Portfolio</a>
            </p>
        </div>
    </footer>

    <script>
        // Space Loading Screen
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('loader').classList.add('hidden');
            }, 1000);
        });

        // Mobile Navigation Toggle
        const navToggle = document.getElementById('navToggle');
        const navLinks = document.getElementById('navLinks');

        navToggle.addEventListener('click', () => {
            navToggle.classList.toggle('active');
            navLinks.classList.toggle('active');
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navToggle.classList.remove('active');
                navLinks.classList.remove('active');
            });
        });

        // Close mobile menu when clicking outside
        document.addEventListener('click', (e) => {
            if (!navToggle.contains(e.target) && !navLinks.contains(e.target)) {
                navToggle.classList.remove('active');
                navLinks.classList.remove('active');
            }
        });

        // Create cosmic particles
        function createCosmicParticles() {
            const particles = document.getElementById('cyberParticles');
            const particleCount = 50;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'cyber-particle';
                
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 8 + 's';
                particle.style.animationDuration = (Math.random() * 4 + 6) + 's';
                
                particles.appendChild(particle);
            }
        }

        // Smooth scrolling
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
        const cosmicObserverOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const cosmicObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('revealed');
                }
            });
        }, cosmicObserverOptions);

        document.querySelectorAll('.scroll-tech-reveal').forEach(element => {
            cosmicObserver.observe(element);
        });

        // Header effects
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('header-active');
            } else {
                header.classList.remove('header-active');
            }
        });

        // Initialize
        createCosmicParticles();

        // Particle regeneration
        setInterval(() => {
            const particles = document.querySelectorAll('.cyber-particle');
            if (particles.length < 30) {
                createCosmicParticles();
            }
        }, 4000);

        // Enhanced mobile experience: prevent scroll when mobile menu is open
        navToggle.addEventListener('click', () => {
            if (navLinks.classList.contains('active')) {
                document.body.style.overflow = '';
            } else {
                document.body.style.overflow = 'hidden';
            }
        });

        // Restore scroll when mobile menu is closed
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                document.body.style.overflow = '';
            });
        });
    </script>
</body>
</html>
