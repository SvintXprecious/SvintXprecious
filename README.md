<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Precious Tsetekani - Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@700;800&display=swap');
        
        :root {
            --primary: #6366f1;
            --secondary: #3b82f6;
            --dark: #1e293b;
            --light: #f8fafc;
            --accent: #ec4899;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.7;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        /* Header Styles */
        header {
            padding: 2rem 0;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            position: relative;
            overflow: hidden;
            border-radius: 0 0 30px 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 2rem;
        }
        
        .profile-container {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }
        
        .profile-pic {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background-color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
            border: 4px solid white;
            overflow: hidden;
        }
        
        .profile-pic img {
            width: 85%;
            height: 85%;
            object-fit: cover;
        }
        
        .profile-info h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            position: relative;
            display: inline-flex;
            align-items: center;
        }
        
        .waving-hand {
            width: 32px;
            height: 32px;
            margin-right: 12px;
        }
        
        .title-emoji {
            width: 40px;
            height: 40px;
            margin-left: 8px;
        }
        
        .profile-info p {
            font-size: 1.1rem;
            opacity: 0.9;
            font-style: italic;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-btn {
            padding: 0.5rem 1rem;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: white;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        
        .social-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
        }
        
        .linkedin {
            background-color: #0077B5;
        }
        
        .discord {
            background-color: #7289da;
        }
        
        .github {
            background-color: #333;
        }
        
        .social-btn i {
            font-size: 1.1rem;
        }
        
        /* Main Content Styles */
        main {
            padding: 3rem 0;
        }
        
        .about-me {
            margin-bottom: 4rem;
        }
        
        .section-title {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            bottom: -8px;
            left: 0;
            border-radius: 2px;
        }
        
        .about-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .about-item {
            background-color: white;
            padding: 1.5rem;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            align-items: flex-start;
            gap: 1rem;
        }
        
        .about-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }
        
        .about-item i {
            font-size: 1.5rem;
            color: var(--primary);
        }
        
        .about-item p {
            margin: 0;
            font-size: 1rem;
        }
        
        .favorites {
            margin-bottom: 4rem;
        }
        
        .favorite-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .favorite-item {
            background-color: white;
            padding: 2rem 1.5rem;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            text-align: center;
        }
        
        .favorite-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }
        
        .favorite-item i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .favorite-item h3 {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
        }
        
        .favorite-item p {
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        .skills-section {
            margin-bottom: 4rem;
        }
        
        .skills-container {
            background-color: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .category {
            margin-bottom: 2rem;
        }
        
        .category:last-child {
            margin-bottom: 0;
        }
        
        .category-title {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .category-title i {
            font-size: 1.4rem;
        }
        
        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }
        
        .skill-badge {
            padding: 0.5rem 1rem;
            border-radius: 50px;
            background-color: #f1f5f9;
            color: var(--dark);
            font-size: 0.9rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .skill-badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
            background-color: #e2e8f0;
        }
        
        .skill-badge i {
            font-size: 1rem;
            color: var(--primary);
        }
        
        /* Contact Section */
        .contact-section {
            margin-bottom: 3rem;
        }
        
        .contact-card {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            color: white;
            text-align: center;
        }
        
        .contact-card h2 {
            margin-bottom: 1rem;
            font-family: 'Montserrat', sans-serif;
        }
        
        .contact-card p {
            margin-bottom: 1.5rem;
            opacity: 0.9;
        }
        
        .contact-email {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background-color: rgba(255, 255, 255, 0.2);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: background-color 0.3s;
        }
        
        .contact-email:hover {
            background-color: rgba(255, 255, 255, 0.3);
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 2rem 0;
            color: #64748b;
            font-size: 0.9rem;
        }
        
        .technologies-marquee {
            overflow: hidden;
            white-space: nowrap;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            border-radius: 12px;
            background-color: white;
            padding: 1.5rem;
            margin-bottom: 4rem;
            position: relative;
        }
        
        .marquee-content {
            display: inline-block;
            animation: marquee 30s linear infinite;
            padding-right: 50px;
        }
        
        .marquee-content:hover {
            animation-play-state: paused;
        }
        
        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
        
        .tech-icon {
            display: inline-flex;
            align-items: center;
            padding: 0.5rem 1rem;
            margin-right: 1rem;
            border-radius: 8px;
            background-color: #f1f5f9;
            font-weight: 500;
            font-size: 0.9rem;
        }
        
        .tech-icon i {
            margin-right: 0.5rem;
            color: var(--primary);
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            .profile-container {
                flex-direction: column;
                margin-bottom: 1.5rem;
            }
            
            .social-links {
                justify-content: center;
            }
            
            .section-title::after {
                left: 50%;
                transform: translateX(-50%);
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="profile-container">
                    <div class="profile-pic">
                        <img src="/api/placeholder/400/320" alt="Profile picture placeholder">
                    </div>
                    <div class="profile-info">
                        <h1>
                            <img class="waving-hand" src="https://raw.githubusercontent.com/ABSphreak/ABSphreak/master/gifs/Hi.gif" alt="Waving hand">
                            Precious Tsetekani
                            <img class="title-emoji" src="/api/placeholder/40/40" alt="Emoji">
                        </h1>
                        <p>Your Friendly Neighbourhood Software Engineer</p>
                    </div>
                </div>
                <div class="social-links">
                    <a href="https://linkedin.com/in/precioustsetekani" class="social-btn linkedin">
                        <i class="fab fa-linkedin-in"></i>
                        LinkedIn
                    </a>
                    <a href="https://discordapp.com/users/svint_x" class="social-btn discord">
                        <i class="fab fa-discord"></i>
                        Tanyx
                    </a>
                    <a href="https://github.com/SvintXprecious/" class="social-btn github">
                        <i class="fab fa-github"></i>
                        Follow
                    </a>
                </div>
            </div>
        </div>
    </header>
    
    <main class="container">
        <section class="about-me">
            <h2 class="section-title">About Me</h2>
            <div class="about-items">
                <div class="about-item">
                    <i class="fas fa-seedling"></i>
                    <p>I'm currently learning <strong>NextJS</strong>.</p>
                </div>
                <div class="about-item">
                    <i class="fas fa-code-branch"></i>
                    <p>Open for collaborations for working on OpenSource projects.</p>
                </div>
                <div class="about-item">
                    <i class="fas fa-handshake"></i>
                    <p>I'm looking to collaborate on making <strong>AI tools</strong>.</p>
                </div>
                <div class="about-item">
                    <i class="fab fa-python"></i>
                    <p>Mostly spends time with Python and Dart.</p>
                </div>
                <div class="about-item">
                    <i class="fas fa-envelope"></i>
                    <p>How to reach me <strong>tsetekaniprecious@gmail.com</strong></p>
                </div>
            </div>
        </section>
        
        <section class="favorites">
            <h2 class="section-title">My Absolute Favorites</h2>
            <div class="favorite-items">
                <div class="favorite-item">
                    <i class="fas fa-laptop-code"></i>
                    <h3>Technology Exploration</h3>
                    <p>I love exploring new technologies and building cool stuff.</p>
                </div>
                <div class="favorite-item">
                    <i class="fas fa-brain"></i>
                    <h3>Problem Solving</h3>
                    <p>Brainstorming on Complex engineering problems.</p>
                </div>
                <div class="favorite-item">
                    <i class="fas fa-pizza-slice"></i>
                    <h3>Tech Community</h3>
                    <p>Hackathons, meetups & tech events.</p>
                </div>
            </div>
        </section>
        
        <section class="technologies-marquee">
            <div class="marquee-content">
                <span class="tech-icon"><i class="fab fa-html5"></i> HTML5</span>
                <span class="tech-icon"><i class="fab fa-js-square"></i> JavaScript</span>
                <span class="tech-icon"><i class="fab fa-react"></i> React</span>
                <span class="tech-icon"><i class="fab fa-node-js"></i> Node.js</span>
                <span class="tech-icon"><i class="fab fa-python"></i> Python</span>
                <span class="tech-icon"><i class="fab fa-aws"></i> AWS</span>
                <span class="tech-icon"><i class="fab fa-docker"></i> Docker</span>
                <span class="tech-icon"><i class="fab fa-figma"></i> Figma</span>
                <span class="tech-icon"><i class="fab fa-git-alt"></i> Git</span>
                <span class="tech-icon"><i class="fas fa-database"></i> MongoDB</span>
            </div>
            <div class="marquee-content">
                <span class="tech-icon"><i class="fab fa-html5"></i> HTML5</span>
                <span class="tech-icon"><i class="fab fa-js-square"></i> JavaScript</span>
                <span class="tech-icon"><i class="fab fa-react"></i> React</span>
                <span class="tech-icon"><i class="fab fa-node-js"></i> Node.js</span>
                <span class="tech-icon"><i class="fab fa-python"></i> Python</span>
                <span class="tech-icon"><i class="fab fa-aws"></i> AWS</span>
                <span class="tech-icon"><i class="fab fa-docker"></i> Docker</span>
                <span class="tech-icon"><i class="fab fa-figma"></i> Figma</span>
                <span class="tech-icon"><i class="fab fa-git-alt"></i> Git</span>
                <span class="tech-icon"><i class="fas fa-database"></i> MongoDB</span>
            </div>
        </section>
        
        <section class="skills-section">
            <h2 class="section-title">Languages and Tools</h2>
            <div class="skills-container">
                <div class="category">
                    <h3 class="category-title"><i class="fas fa-code"></i> Frontend</h3>
                    <div class="skills-grid">
                        <div class="skill-badge"><i class="fab fa-html5"></i> HTML5</div>
                        <div class="skill-badge"><i class="fab fa-js-square"></i> JavaScript</div>
                        <div class="skill-badge"><i class="fab fa-react"></i> React</div>
                        <div class="skill-badge"><i class="fab fa-css3-alt"></i> TailwindCSS</div>
                        <div class="skill-badge"><i class="fab fa-node-js"></i> Next.js</div>
                        <div class="skill-badge"><i class="fab fa-figma"></i> Figma</div>
                        <div class="skill-badge"><i class="fab fa-typescript"></i> TypeScript</div>
                    </div>
                </div>
                
                <div class="category">
                    <h3 class="category-title"><i class="fas fa-server"></i> Backend</h3>
                    <div class="skills-grid">
                        <div class="skill-badge"><i class="fab fa-node-js"></i> Node.js</div>
                        <div class="skill-badge"><i class="fab fa-node-js"></i> Express.js</div>
                        <div class="skill-badge"><i class="fab fa-python"></i> FastAPI</div>
                        <div class="skill-badge"><i class="fas fa-database"></i> MongoDB</div>
                        <div class="skill-badge"><i class="fas fa-database"></i> MySQL</div>
                        <div class="skill-badge"><i class="fas fa-database"></i> PostgreSQL</div>
                    </div>
                </div>
                
                <div class="category">
                    <h3 class="category-title"><i class="fas fa-laptop-code"></i> Languages</h3>
                    <div class="skills-grid">
                        <div class="skill-badge"><i class="fab fa-python"></i> Python</div>
                        <div class="skill-badge"><i class="fab fa-js-square"></i> JavaScript</div>
                        <div class="skill-badge"><i class="fas fa-code"></i> Dart</div>
                        <div class="skill-badge"><i class="fas fa-code"></i> C++</div>
                        <div class="skill-badge"><i class="fab fa-java"></i> Java</div>
                        <div class="skill-badge"><i class="fas fa-terminal"></i> Shell Script</div>
                    </div>
                </div>
                
                <div class="category">
                    <h3 class="category-title"><i class="fas fa-cloud"></i> Cloud & DevOps</h3>
                    <div class="skills-grid">
                        <div class="skill-badge"><i class="fab fa-aws"></i> AWS</div>
                        <div class="skill-badge"><i class="fab fa-docker"></i> Docker</div>
                        <div class="skill-badge"><i class="fab fa-github"></i> GitHub Pages</div>
                        <div class="skill-badge"><i class="fas fa-server"></i> Vercel</div>
                        <div class="skill-badge"><i class="fas fa-cloud"></i> DigitalOcean</div>
                        <div class="skill-badge"><i class="fab fa-firebase"></i> Firebase</div>
                    </div>
                </div>
                
                <div class="category">
                    <h3 class="category-title"><i class="fas fa-brain"></i> AI & Data Science</h3>
                    <div class="skills-grid">
                        <div class="skill-badge"><i class="fab fa-python"></i> NumPy</div>
                        <div class="skill-badge"><i class="fab fa-python"></i> Pandas</div>
                        <div class="skill-badge"><i class="fas fa-chart-line"></i> Matplotlib</div>
                        <div class="skill-badge"><i class="fas fa-brain"></i> TensorFlow</div>
                        <div class="skill-badge"><i class="fas fa-brain"></i> PyTorch</div>
                        <div class="skill-badge"><i class="fas fa-cogs"></i> scikit-learn</div>
                        <div class="skill-badge"><i class="fas fa-project-diagram"></i> mlflow</div>
                    </div>
                </div>
                
                <div class="category">
                    <h3 class="category-title"><i class="fas fa-toolbox"></i> Tools</h3>
                    <div class="skills-grid">
                        <div class="skill-badge"><i class="fab fa-git-alt"></i> Git</div>
                        <div class="skill-badge"><i class="fab fa-npm"></i> NPM</div>
                        <div class="skill-badge"><i class="fas fa-bug"></i> Postman</div>
                        <div class="skill-badge"><i class="fab fa-figma"></i> Figma</div>
                        <div class="skill-badge"><i class="fas fa-palette"></i> Canva</div>
                        <div class="skill-badge"><i class="fab fa-windows"></i> Windows Terminal</div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="contact-section">
            <div class="contact-card">
                <h2>Let's Connect!</h2>
                <p>Open for collaboration and interesting projects. Feel free to reach out.</p>
                <a href="mailto:tsetekaniprecious@gmail.com" class="contact-email">
                    <i class="fas fa-envelope"></i>
                    tsetekaniprecious@gmail.com
                </a>
            </div>
        </section>
    </main>
    
    <footer class="container">
        <p>© 2025 Precious Tsetekani | Software Engineer | AI Enthusiast</p>
    </footer>
</body>
</html>
