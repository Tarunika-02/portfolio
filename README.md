<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tarunika T | Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
    :root {
            --primary-color: #0A0A0A;
            --secondary-color: #121212;
            --accent-color: #1DB954;
            --accent-hover: #1ed760;
            --text-primary: #FFFFFF;
            --text-secondary: #B3B3B3;
            --background: #000000;
            --card-background: #181818;
            --border-color: #282828;
            --section-spacing: 120px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--background);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Modern Navigation */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            backdrop-filter: blur(12px);
            padding: 1.5rem 2rem;
            z-index: 1000;
            border-bottom: 1px solid rgba(40, 40, 40, 0.5);
            transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
            box-shadow: 0 5px 20px rgba(29, 185, 84, 0.1);
        }

        .navbar.scrolled {
            padding: 1rem 2rem;
            background-color: rgba(0, 0, 0, 0.95);
        }

        .nav-content {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--text-primary), var(--accent-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 1rem;
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
            background: var(--accent-color);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--text-primary);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a.active {
            color: var(--text-primary);
        }

        .nav-links a.active::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            cursor: pointer;
            color: var(--text-primary);
            font-size: 1.5rem;
        }

        /* Hero Section with Particle Background */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 2rem;
            overflow: hidden;
        }
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
        }

        .particle {
            position: absolute;
            background-color: var(--accent-color);
            border-radius: 50%;
            opacity: 0.5;
        }

               .hero {
            position: relative;
            overflow: hidden;
        }
        
   .background-title {
        position: absolute;
        font-size: 12vw;
        font-weight: 900;
        color: rgba(29, 185, 84, 0.15); /* Darker green with 15% opacity */
        text-transform: uppercase;
        z-index: 1;
        pointer-events: none;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        text-align: center;
        line-height: 0.8;
    }
    .background-title span {
        display: block;
    }
        
    .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
            width: 100%;
        }

        .hero h1 {
            font-size: 4.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.1;
            font-weight: 800;
            background: linear-gradient(to right, var(--text-primary), var(--accent-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 20px rgba(29, 185, 84, 0.3);
        }

        .hero p {
            font-size: 1.4rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto 3rem;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        /* Typewriter Effect */
        .typewriter {
            display: inline-block;
            position: relative;
        }

        .typewriter::after {
            content: '|';
            position: absolute;
            right: -10px;
            animation: blink 1s infinite;
            color: #1DB954;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }

        /* Glowing Button */
        .glow-button {
            position: relative;
            padding: 1.2rem 2.5rem;
            background: linear-gradient(90deg, var(--accent-color), var(--accent-hover));
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            overflow: hidden;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 10px 30px -10px var(--accent-color);
            z-index: 1;
        }

        .glow-button:hover {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 15px 40px -10px var(--accent-color);
        }

        .glow-button.secondary {
            background: transparent;
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--text-primary);
            box-shadow: none;
        }

        .glow-button.secondary:hover {
            border-color: var(--accent-color);
            color: var(--accent-color);
        }

        /* Section Styles */
        section {
            padding: var(--section-spacing) 2rem;
            position: relative;
        }

        .section-header {
            font-size: 3rem;
            margin-bottom: 4rem;
            font-weight: 700;
            position: relative;
            display: inline-block;
            text-shadow: 0 0 10px rgba(29, 185, 84, 0.3);
        }

        .section-header::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 0;
            width: 60px;
            height: 4px;
            background: var(--accent-color);
            border-radius: 2px;
        }

        /* About Section */
        .about {
            background-color: var(--primary-color);
        }

        .about-content {
            max-width: 1400px;
            margin: 0 auto;
        }

        .about-text {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .about-text p {
            color: var(--text-secondary);
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Skill Tags with Progress Bars */
        .skills-container {
            margin-top: 2rem;
        }

        .skill-item {
            margin-bottom: 1.5rem;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .skill-name {
            font-weight: 500;
        }

        .skill-percent {
            color: var(--accent-color);
        }

        .skill-bar {
            height: 8px;
            background-color: var(--secondary-color);
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, var(--accent-color), var(--accent-hover));
            border-radius: 4px;
            width: 0;
            transition: width 1.5s ease;
            box-shadow: 0 0 10px rgba(29, 185, 84, 0.3);
        }

        /* Projects Section with Hover Effects */
        .projects {
            background-color: var(--background);
        }

        .projects-content {
            max-width: 1400px;
            margin: 0 auto;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2.5rem;
        }

        .project-card {
            position: relative;
            background: linear-gradient(145deg, var(--card-background), var(--primary-color));
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275), box-shadow 0.3s ease;
            border: 1px solid var(--border-color);
            box-shadow: 0 20px 40px -15px rgba(0, 0, 0, 0.3);
        }

        .project-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 30px 60px -15px rgba(29, 185, 84, 0.4);
        }

        .project-image-container {
            position: relative;
            overflow: hidden;
            height: 300px;
        }

        .project-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.8s ease;
        }

        .project-card:hover .project-image {
            transform: scale(1.05);
        }

        .project-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.9), transparent);
            opacity: 0;
            transition: opacity 0.3s ease;
            display: flex;
            align-items: flex-end;
            padding: 2rem;
        }

        .project-card:hover .project-overlay {
            opacity: 1;
        }

        .project-info {
            padding: 2rem;
        }

        .project-info h3 {
            margin-bottom: 1rem;
            color: var(--text-primary);
            font-size: 1.5rem;
            font-weight: 600;
        }

        .project-info p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-bottom: 1.5rem;
        }

        .project-tag {
            padding: 0.4rem 0.8rem;
            background: rgba(29, 185, 84, 0.1);
            color: var(--accent-color);
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
            box-shadow: 0 0 8px rgba(29, 185, 84, 0.2);
        }

        /* Experience Section */
        .experience {
            background-color: var(--primary-color);
        }

        .experience-content {
            max-width: 1400px;
            margin: 0 auto;
        }

        .experience-item {
            background: linear-gradient(145deg, var(--card-background), var(--primary-color));
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
        }

        .experience-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px -15px rgba(29, 185, 84, 0.3);
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .experience-title {
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--text-primary);
        }

        .experience-date {
            color: var(--accent-color);
            font-weight: 500;
        }

        .experience-description {
            color: var(--text-secondary);
            line-height: 1.7;
        }

        /* Contact Section with Contact Methods */
        .contact {
            background-color: var(--background);
        }

        .contact-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-description {
            font-size: 1.2rem;
            color: var(--text-secondary);
            margin-bottom: 3rem;
            line-height: 1.7;
        }

        .contact-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .contact-method {
            background: linear-gradient(145deg, var(--card-background), var(--primary-color));
            border-radius: 20px;
            padding: 2rem;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
            text-align: center;
        }

        .contact-method:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px -15px rgba(29, 185, 84, 0.3);
        }

        .contact-icon-link {
            display: block;
            text-decoration: none;
            color: inherit;
        }

        .contact-icon-link:hover .contact-icon {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px -10px var(--accent-color);
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background: var(--accent-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem;
            font-size: 1.5rem;
            color: var(--text-primary);
            transition: all 0.3s ease;
        }

        .contact-details h3 {
            color: var(--text-primary);
            margin-bottom: 0.5rem;
            font-size: 1.2rem;
        }

        .contact-details a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-details a:hover {
            color: var(--accent-color);
        }

        /* Footer with Wave Design */
        .footer {
            position: relative;
            padding: 6rem 2rem 2rem;
            background-color: var(--primary-color);
            text-align: center;
        }

        .footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100px;
            background: url("data:image/svg+xml,%3Csvg viewBox='0 0 1200 120' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z' fill='%23121212' opacity='.25'/%3E%3Cpath d='M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z' fill='%231DB954' opacity='0.3'/%3E%3C/svg%3E");
            background-size: cover;
            background-repeat: no-repeat;
            transform: rotate(180deg);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: var(--card-background);
            border-radius: 50%;
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 1.2rem;
            transition: all 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 0 10px rgba(29, 185, 84, 0);
        }

        .social-links a:hover {
            background: var(--accent-color);
            color: var(--text-primary);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px -10px var(--accent-color), 0 0 20px rgba(29, 185, 84, 0.5);
        }

        .footer p {
            color: var(--text-secondary);
            margin-top: 1.5rem;
        }

        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            background: var(--accent-color);
            color: var(--text-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 999;
            box-shadow: 0 5px 15px rgba(29, 185, 84, 0.5);
        }

        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(29, 185, 84, 0.7);
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .delay-1 {
            transition-delay: 0.1s;
        }

        .delay-2 {
            transition-delay: 0.2s;
        }

        .delay-3 {
            transition-delay: 0.3s;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            :root {
                --section-spacing: 80px;
            }
            
           .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            line-height: 1.1;
            font-weight: 800;
            background: linear-gradient(to right, var(--text-primary), var(--accent-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto 3rem;
        }
            
            .section-header {
                font-size: 2.5rem;
                margin-bottom: 3rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .project-grid {
                grid-template-columns: 1fr;
            }
            
         .hero-buttons {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            margin-top: 2rem;
        }
            
            .glow-button {
                width: 100%;
                max-width: 300px;
                text-align: center;
            }

            .experience-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.5rem;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section-header {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-content">
            <a href="#" class="logo">Tarunika T</a>
            <div class="nav-links">
                <a href="#home" class="active">Home</a>
                <a href="#about">About</a>
                <a href="#experience">Experience</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </div>
            <div class="menu-toggle">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </nav>

 <!-- Hero Section -->
<section id="home" class="hero">
         <div class="background-title">
        <span>GRAPHIC</span>
        <span>DESIGNER</span>
    </div>
        <div class="particles" id="particles-js"></div>
        <div class="hero-content">
            <h1 class="fade-in">Hi, I'm Tarunika T</h1><br>
            <p class="fade-in delay-1"> A 'BCA' Graduate with a strong academic background and hands-on experience in graphic design, UI/UX, and web development. Passionate about designing visually appealing and functional digital experiences.</p>
            <div class="hero-buttons fade-in delay-2">
                <button class="glow-button" onclick="document.getElementById('projects').scrollIntoView({behavior: 'smooth'})">View My Work</button>
                <button class="glow-button secondary" onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'})">Let's Connect</button>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="about-content">
            <div class="about-text fade-in">
                <h2 class="section-header">About Me</h2>
                <p>I'm a BCA Graduate with a passion for creating beautiful and functional digital experiences. With expertise in graphic design, UI/UX, and web development, I bring ideas to life through clean code and intuitive design.</p>
                <p>My journey in design and development has been driven by creative problem-solving and modern development tools. I'm eager to contribute innovative ideas, collaborate with experts, and grow in the dynamic field of design and web development.</p>
                
                <div class="skills-container">
                    <div class="skill-item">
                        <div class="skill-info">
                            <span class="skill-name">HTML/CSS</span>
                            <span class="skill-percent">90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="90"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-info">
                            <span class="skill-name">JavaScript</span>
                            <span class="skill-percent">85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-info">
                            <span class="skill-name">Python</span>
                            <span class="skill-percent">80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="80"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-info">
                            <span class="skill-name">Power BI</span>
                            <span class="skill-percent">85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="85"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-info">
                            <span class="skill-name">Graphic Design</span>
                            <span class="skill-percent">90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="90"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-info">
                            <span class="skill-name">Data Science</span>
                            <span class="skill-percent">75%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" data-width="75"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="experience-content">
            <h2 class="section-header fade-in">Experience</h2>
            
            <div class="experience-item fade-in">
                <div class="experience-header">
                    <div>
                        <h3 class="experience-title">Graphic Designing Intern</h3>
                    </div>
                    <div class="experience-date">Feb 2025 - May 2025</div>
                </div>
                <p class="experience-description">Created visually compelling designs to enhance brand appeal and user engagement. Delivered polished graphics and layouts while meeting deadlines and client expectations.</p>
            </div>

            <div class="experience-item fade-in delay-1">
                <div class="experience-header">
                    <div>
                        <h3 class="experience-title">Grounds Crew Member</h3>
                    </div>
                    <div class="experience-date">Jun 2023 - Nov 2023</div>
                </div>
                <p class="experience-description">Developed and implemented strategies to increase sales and profitability. Provided regular financial reporting on budgeting, forecasting, and performance metrics.</p>
            </div>

            <div class="experience-item fade-in delay-2">
                <div class="experience-header">
                    <div>
                        <h3 class="experience-title">Digital Marketing Intern</h3>
                    </div>
                    <div class="experience-date">Sep 2023 - Oct 2023</div>
                </div>
                <p class="experience-description">Worked in a team of digital marketing, specializing in creating compelling content. Expertise included developing and executing impactful social media campaigns, targeted email marketing initiatives, and innovative website designs.</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="projects-content">
            <h2 class="section-header fade-in">My Projects</h2>
            <div class="project-grid">
                <div class="project-card fade-in">
                    <div class="project-image-container">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Power BI Training Portal" class="project-image">
                        <div class="project-overlay">
                            <button class="glow-button" onclick="window.open('https://e2emgmtservices.github.io/-powerbi/', '_blank')">View Project</button>
                        </div>
                    </div>
                    <div class="project-info">
                        <h3>Power BI Training Portal</h3>
                        <p>Power BI Analytics Training Platform: Interactive courses, student testimonials, and seamless enrollment, built with modern web technologies for an engaging learning experience.</p>
                        <div class="project-tags">
                            <span class="project-tag">HTML5</span>
                            <span class="project-tag">CSS3</span>
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">Tailwind CSS</span>
                            <span class="project-tag">Responsive Design</span>
                        </div>
                    </div>
                </div>
                <div class="project-card fade-in delay-1">
                    <div class="project-image-container">
                        <img src="https://images.unsplash.com/photo-1517077304055-6e89abbf09b0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="CodeLearn Platform" class="project-image">
                        <div class="project-overlay">
                            <button class="glow-button">View Project</button>
                        </div>
                    </div>
                    <div class="project-info">
                        <h3>CodeLearn Platform</h3>
                        <p>CodeLearn is an interactive platform designed to make learning to code exciting, engaging, and accessible through mini-games, challenges, and quizzes. It transforms complex programming concepts into playful experiences.</p>
                        <div class="project-tags">
                            <span class="project-tag">HTML</span>
                            <span class="project-tag">CSS</span>
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">PHP</span>
                            <span class="project-tag">MySQL</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="contact-content">
            <h2 class="section-header fade-in">Get In Touch</h2>
            <div class="contact-info fade-in delay-1">
                <p class="contact-description">Feel free to reach out to me through any of the following platforms. I'm always open to discussing new opportunities, collaborations, or just having a friendly chat about design and development!</p>
                <div class="contact-methods">
                    <div class="contact-method">
                        <a href="mailto:tarunika2817@gmail.com" class="contact-icon-link">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                        </a>
                        <div class="contact-details">
                            <h3>Email</h3>
                            <a href="mailto:tarunika2817@gmail.com">tarunika2817@gmail.com</a>
                        </div>
                    </div>
                    <div class="contact-method">
                        <a href="https://www.linkedin.com/in/tarunika-t-76215b250" target="_blank" class="contact-icon-link">
                            <div class="contact-icon">
                                <i class="fab fa-linkedin-in"></i>
                            </div>
                        </a>
                        <div class="contact-details">
                            <h3>LinkedIn</h3>
                            <a href="https://www.linkedin.com/in/tarunika-t-76215b250" target="_blank">tarunika-t-76215b250</a>
                        </div>
                    </div>
                    <div class="contact-method">
                        <a href="https://t.me/Tarunika_2851" target="_blank" class="contact-icon-link">
                            <div class="contact-icon">
                                <i class="fab fa-telegram-plane"></i>
                            </div>
                        </a>
                        <div class="contact-details">
                            <h3>Telegram</h3>
                            <a href="https://t.me/Tarunika_2851" target="_blank">@Tarunika_2851</a>
                        </div>
                    </div>
                    <div class="contact-method">
                        <a href="https://www.instagram.com/tarunika_02_" target="_blank" class="contact-icon-link">
                            <div class="contact-icon">
                                <i class="fab fa-instagram"></i>
                            </div>
                        </a>
                        <div class="contact-details">
                            <h3>Instagram</h3>
                            <a href="https://www.instagram.com/tarunika_02_" target="_blank">@tarunika_02_</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="social-links fade-in">
            <a href="https://www.linkedin.com/in/tarunika-t-76215b250" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
            <a href="mailto:tarunika2817@gmail.com" aria-label="Email"><i class="fas fa-envelope"></i></a>
            <a href="https://t.me/Tarunika_2851" target="_blank" aria-label="Telegram"><i class="fab fa-telegram-plane"></i></a>
            <a href="https://www.instagram.com/tarunika_02_" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
        </div>
        <p class="fade-in delay-1">&copy; 2025 Tarunika T. All rights reserved.</p>
    </footer>

    <!-- Back to Top Button -->
    <a href="#home" class="back-to-top" id="back-to-top">
        <i class="fas fa-arrow-up"></i>
    </a>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Active nav link on scroll
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-links a');

        window.addEventListener('scroll', function() {
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (pageYOffset >= (sectionTop - 300)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });

        // Mobile menu toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinksContainer = document.querySelector('.nav-links');

        menuToggle.addEventListener('click', function() {
            navLinksContainer.classList.toggle('active');
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            // Skip for back-to-top button
            if (anchor.id === 'back-to-top') return;
            
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Back to top button functionality
        const backToTop = document.getElementById('back-to-top');
        backToTop.addEventListener('click', function(e) {
            e.preventDefault();
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        // Show/hide back-to-top button based on scroll position
        window.addEventListener('scroll', function() {
            if (window.pageYOffset > 300) {
                backToTop.classList.add('visible');
            } else {
                backToTop.classList.remove('visible');
            }
        });

        // Intersection Observer for animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    
                    // Animate skill bars
                    if (entry.target.classList.contains('about-text')) {
                        document.querySelectorAll('.skill-progress').forEach(bar => {
                            const width = bar.getAttribute('data-width');
                            bar.style.width = width + '%';
                        });
                    }
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.fade-in').forEach(element => {
            observer.observe(element);
        });

        // Particle background
        function createParticles() {
            const particlesContainer = document.getElementById('particles-js');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random size between 2px and 6px
                const size = Math.random() * 4 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                // Random position
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100}%`;
                
                // Random animation
                const duration = Math.random() * 20 + 10;
                const delay = Math.random() * 5;
                particle.style.animation = `float ${duration}s ease-in-out ${delay}s infinite`;
                
                particlesContainer.appendChild(particle);
            }
        }

        // Create particles when page loads
        window.addEventListener('load', createParticles);

        // CSS animation for particles
        const style = document.createElement('style');
        style.textContent = `
            @keyframes float {
                0%, 100% {
                    transform: translateY(0px) rotate(0deg);
                    opacity: 0.5;
                }
                50% {
                    transform: translateY(-20px) rotate(180deg);
                    opacity: 1;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
