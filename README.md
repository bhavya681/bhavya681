<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bhavya Wade - MERN Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&family=Exo+2:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #00F718;
            --secondary: #8A2BE2;
            --accent: #FF00FF;
            --dark: #0a0a14;
            --darker: #050510;
            --light: #f0f0f0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Exo 2', sans-serif;
            background-color: var(--darker);
            color: var(--light);
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(138, 43, 226, 0.1) 0%, transparent 20%),
                radial-gradient(circle at 90% 80%, rgba(0, 247, 24, 0.1) 0%, transparent 20%);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            padding: 30px 0;
            position: relative;
            text-align: center;
            margin-bottom: 40px;
            overflow: hidden;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        .profile-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            font-weight: 900;
            margin-bottom: 15px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 15px rgba(0, 247, 24, 0.5);
            letter-spacing: 2px;
        }
        
        .profile-subtitle {
            font-size: 1.8rem;
            color: var(--light);
            margin-bottom: 30px;
            font-weight: 600;
            text-shadow: 0 0 10px rgba(138, 43, 226, 0.7);
        }
        
        .profile-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin: 0 auto 20px;
            border: 5px solid var(--primary);
            box-shadow: 
                0 0 20px var(--primary),
                0 0 40px rgba(138, 43, 226, 0.5);
            position: relative;
            overflow: hidden;
            background: linear-gradient(45deg, var(--darker), var(--dark));
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .profile-image i {
            font-size: 6rem;
            color: var(--primary);
        }
        
        .glowing-border {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            box-shadow: 
                inset 0 0 20px var(--primary),
                0 0 30px var(--primary);
            animation: glow 3s ease-in-out infinite alternate;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-box {
            background: rgba(15, 15, 35, 0.7);
            border: 1px solid var(--primary);
            border-radius: 10px;
            padding: 15px 25px;
            text-align: center;
            box-shadow: 0 0 15px rgba(0, 247, 24, 0.3);
            backdrop-filter: blur(5px);
        }
        
        .stat-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            font-family: 'Orbitron', sans-serif;
        }
        
        .stat-label {
            font-size: 1rem;
            color: var(--light);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        /* Sections */
        section {
            padding: 50px 0;
            position: relative;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title h2 {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            font-weight: 700;
            display: inline-block;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 10px rgba(0, 247, 24, 0.3);
            position: relative;
            z-index: 2;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
            box-shadow: 0 0 10px var(--primary);
        }
        
        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
            background: rgba(10, 10, 30, 0.7);
            border: 1px solid var(--primary);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 0 30px rgba(0, 247, 24, 0.2);
            backdrop-filter: blur(10px);
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
            line-height: 1.8;
            color: #e0e0e0;
        }
        
        .about-highlights {
            flex: 1;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }
        
        .highlight-card {
            background: rgba(15, 15, 35, 0.8);
            border: 1px solid var(--secondary);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
        }
        
        .highlight-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(138, 43, 226, 0.3);
        }
        
        .highlight-card i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .highlight-card h3 {
            color: var(--light);
            margin-bottom: 10px;
            font-size: 1.3rem;
        }
        
        .highlight-card p {
            color: #b0b0b0;
            font-size: 0.95rem;
        }
        
        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: rgba(10, 10, 30, 0.7);
            border: 1px solid var(--primary);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s ease;
            position: relative;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 247, 24, 0.3);
        }
        
        .project-header {
            background: linear-gradient(90deg, var(--dark), var(--darker));
            padding: 20px;
            border-bottom: 2px solid var(--primary);
        }
        
        .project-header h3 {
            font-size: 1.5rem;
            color: var(--primary);
            font-family: 'Orbitron', sans-serif;
            margin-bottom: 10px;
        }
        
        .project-header p {
            color: var(--light);
            font-size: 1.1rem;
        }
        
        .project-body {
            padding: 20px;
        }
        
        .project-features {
            list-style: none;
            margin: 20px 0;
        }
        
        .project-features li {
            padding: 8px 0;
            padding-left: 30px;
            position: relative;
            color: #d0d0d0;
        }
        
        .project-features li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--primary);
            font-weight: bold;
        }
        
        .project-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .project-link {
            flex: 1;
            text-align: center;
            padding: 12px;
            background: var(--primary);
            color: var(--darker);
            border-radius: 5px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            font-family: 'Orbitron', sans-serif;
            letter-spacing: 1px;
        }
        
        .project-link:hover {
            background: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.4);
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .skill-category {
            background: rgba(10, 10, 30, 0.7);
            border: 1px solid var(--secondary);
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.2);
        }
        
        .skill-category h3 {
            color: var(--primary);
            margin-bottom: 20px;
            font-family: 'Orbitron', sans-serif;
            font-size: 1.5rem;
            text-align: center;
            position: relative;
        }
        
        .skill-category h3::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background: var(--primary);
            border-radius: 2px;
        }
        
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-top: 25px;
        }
        
        .skill-item {
            background: rgba(20, 20, 40, 0.8);
            border: 1px solid var(--primary);
            border-radius: 30px;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            background: var(--primary);
            color: var(--darker);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 247, 24, 0.3);
        }
        
        .skill-item i {
            font-size: 1.2rem;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .contact-info {
            background: rgba(10, 10, 30, 0.7);
            border: 1px solid var(--primary);
            border-radius: 15px;
            padding: 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 25px;
            padding-bottom: 25px;
            border-bottom: 1px solid rgba(0, 247, 24, 0.2);
        }
        
        .contact-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        .contact-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: rgba(0, 247, 24, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .contact-details h4 {
            color: var(--light);
            margin-bottom: 5px;
            font-size: 1.3rem;
        }
        
        .contact-details p, .contact-details a {
            color: #b0b0b0;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .contact-details a:hover {
            color: var(--primary);
            text-shadow: 0 0 10px rgba(0, 247, 24, 0.5);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(138, 43, 226, 0.1);
            color: var(--secondary);
            font-size: 1.5rem;
            border: 2px solid var(--secondary);
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background: var(--secondary);
            color: var(--light);
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.4);
        }
        
        /* Footer */
        footer {
            padding: 50px 0 30px;
            text-align: center;
            border-top: 1px solid rgba(0, 247, 24, 0.2);
            margin-top: 50px;
        }
        
        .footer-logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
            display: inline-block;
            text-shadow: 0 0 15px rgba(0, 247, 24, 0.3);
        }
        
        .footer-text {
            color: #b0b0b0;
            max-width: 600px;
            margin: 0 auto 30px;
            font-size: 1.1rem;
        }
        
        .copyright {
            color: #888;
            font-size: 0.9rem;
            margin-top: 30px;
        }
        
        /* Animations */
        @keyframes glow {
            0% {
                box-shadow: 
                    inset 0 0 20px var(--primary),
                    0 0 30px var(--primary);
            }
            100% {
                box-shadow: 
                    inset 0 0 30px var(--primary),
                    0 0 50px var(--primary),
                    0 0 70px var(--secondary);
            }
        }
        
        @keyframes float {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
            100% {
                transform: translateY(0);
            }
        }
        
        .floating {
            animation: float 4s ease-in-out infinite;
        }
        
        /* Particles */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }
        
        .particle {
            position: absolute;
            border-radius: 50%;
            background: var(--primary);
            opacity: 0.7;
            box-shadow: 0 0 10px var(--primary);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .header-title {
                font-size: 2.8rem;
            }
            
            .header-subtitle {
                font-size: 1.5rem;
            }
        }
        
        @media (max-width: 768px) {
            .header-title {
                font-size: 2.3rem;
            }
            
            .header-subtitle {
                font-size: 1.3rem;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .stat-box {
                width: 80%;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="particles" id="particles"></div>
        <div class="container header-content">
            <div class="profile-image floating">
                <div class="glowing-border"></div>
                <i class="fas fa-code"></i>
            </div>
            <h1 class="profile-title">🚀 Bhavya Wade</h1>
            <h2 class="profile-subtitle">MERN Stack Developer</h2>
            
            <div class="stats">
                <div class="stat-box">
                    <div class="stat-value">5+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value">15+</div>
                    <div class="stat-label">Technologies</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value">100%</div>
                    <div class="stat-label">Passion</div>
                </div>
            </div>
        </div>
    </header>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            
            <div class="about-content">
                <div class="about-text">
                    <p>Passionate MERN Stack Developer from India with expertise in building modern web applications using cutting-edge technologies.</p>
                    <p>I specialize in creating seamless, scalable, and engaging web experiences that solve real-world problems and deliver exceptional user experiences.</p>
                    <p>Constantly exploring new technologies and methodologies to enhance my skills and deliver innovative solutions that push boundaries.</p>
                </div>
                
                <div class="about-highlights">
                    <div class="highlight-card">
                        <i class="fas fa-bolt"></i>
                        <h3>Fast & Efficient</h3>
                        <p>Optimized applications with lightning-fast performance</p>
                    </div>
                    <div class="highlight-card">
                        <i class="fas fa-layer-group"></i>
                        <h3>Modern Stacks</h3>
                        <p>Expert in MERN, Next.js, TypeScript and more</p>
                    </div>
                    <div class="highlight-card">
                        <i class="fas fa-shield-alt"></i>
                        <h3>Secure</h3>
                        <p>Enterprise-grade security for all applications</p>
                    </div>
                    <div class="highlight-card">
                        <i class="fas fa-mobile-alt"></i>
                        <h3>Responsive</h3>
                        <p>Fully responsive designs for all devices</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" style="background: rgba(5, 5, 15, 0.5);">
        <div class="container">
            <div class="section-title">
                <h2>Featured Projects</h2>
            </div>
            
            <div class="projects-grid">
                <!-- TrialTailTender -->
                <div class="project-card">
                    <div class="project-header">
                        <h3>TrialTailTender</h3>
                        <p>Smart Pet Care Ecosystem</p>
                    </div>
                    <div class="project-body">
                        <p>A comprehensive platform connecting pet owners with trusted sitters and breeders.</p>
                        <ul class="project-features">
                            <li>Pet profile management</li>
                            <li>Sitter booking system</li>
                            <li>Community forum</li>
                            <li>Real-time chat</li>
                            <li>Location-based recommendations</li>
                        </ul>
                        <div class="project-links">
                            <a href="https://trialtailtender-xiab-one.vercel.app/" class="project-link" target="_blank">Live Demo</a>
                            <a href="https://github.com/bhavya681/TrialTailTender" class="project-link" target="_blank">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- LearnNova -->
                <div class="project-card">
                    <div class="project-header">
                        <h3>LearnNova</h3>
                        <p>Interactive Learning Platform</p>
                    </div>
                    <div class="project-body">
                        <p>An educational platform with interactive courses and coding challenges.</p>
                        <ul class="project-features">
                            <li>Interactive coding environment</li>
                            <li>Course progress tracking</li>
                            <li>Skill assessments</li>
                            <li>Community support</li>
                            <li>Certification system</li>
                        </ul>
                        <div class="project-links">
                            <a href="https://learnova1.vercel.app/" class="project-link" target="_blank">Live Demo</a>
                            <a href="https://github.com/bhavya681/LearnNova" class="project-link" target="_blank">GitHub</a>
                        </div>
                    </div>
                </div>
                
                <!-- Code Buddy -->
                <div class="project-card">
                    <div class="project-header">
                        <h3>Code Buddy</h3>
                        <p>Developer Social Network</p>
                    </div>
                    <div class="project-body">
                        <p>A social platform for developers to connect, collaborate, and share knowledge.</p>
                        <ul class="project-features">
                            <li>Developer profiles</li>
                            <li>Project showcase</li>
                            <li>Code collaboration</li>
                            <li>Tech discussions</li>
                            <li>Job board</li>
                        </ul>
                        <div class="project-links">
                            <a href="https://codebuddy-gamma.vercel.app/" class="project-link" target="_blank">Live Demo</a>
                            <a href="https://github.com/bhavya681/CodeBuddy" class="project-link" target="_blank">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>Technical Skills</h2>
            </div>
            
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Frontend</h3>
                    <div class="skills-list">
                        <div class="skill-item">
                            <i class="fab fa-react"></i>
                            <span>ReactJS</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-js"></i>
                            <span>JavaScript</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-html5"></i>
                            <span>HTML5</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-css3-alt"></i>
                            <span>CSS3</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-vuejs"></i>
                            <span>Vue.js</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-sass"></i>
                            <span>SASS</span>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Backend</h3>
                    <div class="skills-list">
                        <div class="skill-item">
                            <i class="fab fa-node-js"></i>
                            <span>Node.js</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-server"></i>
                            <span>Express.js</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-database"></i>
                            <span>MongoDB</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-database"></i>
                            <span>Redis</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-fire"></i>
                            <span>Firebase</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-cloud"></i>
                            <span>REST APIs</span>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Tools & DevOps</h3>
                    <div class="skills-list">
                        <div class="skill-item">
                            <i class="fab fa-git-alt"></i>
                            <span>Git</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-docker"></i>
                            <span>Docker</span>
                        </div>
                        <div class="skill-item">
                            <i class="fab fa-linux"></i>
                            <span>Linux</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-terminal"></i>
                            <span>CLI</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-shield-alt"></i>
                            <span>BurpSuite</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-code"></i>
                            <span>VS Code</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" style="background: rgba(5, 5, 15, 0.5);">
        <div class="container">
            <div class="section-title">
                <h2>Connect With Me</h2>
            </div>
            
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Email</h4>
                            <a href="mailto:bhavyawade2@gmail.com">bhavyawade2@gmail.com</a>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Portfolio</h4>
                            <a href="https://bhavyawade.vercel.app/" target="_blank">bhavyawade.vercel.app</a>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Location</h4>
                            <p>India</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-info">
                    <h3 style="color: var(--primary); text-align: center; margin-bottom: 30px; font-family: 'Orbitron', sans-serif;">Social Profiles</h3>
                    <div style="text-align: center;">
                        <div class="social-links">
                            <a href="https://github.com/bhavya681" class="social-link" target="_blank">
                                <i class="fab fa-github"></i>
                            </a>
                            <a href="https://www.linkedin.com/in/bhavya-wade/" class="social-link" target="_blank">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                            <a href="https://x.com/wade_bhavy55123" class="social-link" target="_blank">
                                <i class="fab fa-twitter"></i>
                            </a>
                            <a href="https://bhavyawade-hswa.vercel.app/" class="social-link" target="_blank">
                                <i class="fas fa-external-link-alt"></i>
                            </a>
                        </div>
                        <p style="margin-top: 30px; color: #b0b0b0;">
                            Let's connect and build something amazing together!
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-logo">Bhavya Wade</div>
            <p class="footer-text">MERN Stack Developer specializing in creating modern, scalable web applications with cutting-edge technologies.</p>
            
            <div class="social-links" style="justify-content: center;">
                <a href="https://github.com/bhavya681" class="social-link" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://www.linkedin.com/in/bhavya-wade/" class="social-link" target="_blank">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://x.com/wade_bhavy55123" class="social-link" target="_blank">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="https://bhavyawade.vercel.app/" class="social-link" target="_blank">
                    <i class="fas fa-globe"></i>
                </a>
            </div>
            
            <p class="copyright">© 2023 Bhavya Wade. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Create particles
        document.addEventListener('DOMContentLoaded', function() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random position
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                
                // Random size
                const size = Math.random() * 5 + 1;
                
                // Random color (green or purple)
                const color = Math.random() > 0.5 ? 'var(--primary)' : 'var(--secondary)';
                
                // Set styles
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.backgroundColor = color;
                particle.style.left = `${posX}%`;
                particle.style.top = `${posY}%`;
                
                // Random animation
                const duration = Math.random() * 10 + 5;
                const delay = Math.random() * 5;
                particle.style.animation = `float ${duration}s infinite ${delay}s`;
                
                particlesContainer.appendChild(particle);
            }
            
            // Add hover effect to project cards
            const projectCards = document.querySelectorAll('.project-card');
            projectCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.boxShadow = '0 15px 30px rgba(0, 247, 24, 0.4)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.3)';
                });
            });
        });
    </script>
</body>
</html>
