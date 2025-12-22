<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Eron Bruti | Full-Stack Architect</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0066cc;
            --primary-dark: #0052a3;
            --secondary: #2d3748;
            --accent: #00bfff;
            --light: #f8fafc;
            --dark: #1a202c;
            --gray: #718096;
            --light-gray: #e2e8f0;
            --border-radius: 8px;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.07);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: #f9fafb;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .container {
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            overflow: hidden;
        }
        
        /* Header Section */
        .header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 3rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.05'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }
        
        .profile-header {
            position: relative;
            z-index: 2;
        }
        
        .name-title {
            font-size: 2.8rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            letter-spacing: -0.5px;
        }
        
        .tagline {
            font-size: 1.4rem;
            font-weight: 300;
            margin-bottom: 1.5rem;
            opacity: 0.9;
        }
        
        .specialties {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .specialty {
            background: rgba(255, 255, 255, 0.15);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            font-weight: 500;
            font-size: 0.95rem;
            backdrop-filter: blur(5px);
        }
        
        /* Main Content */
        .content {
            display: flex;
            flex-wrap: wrap;
            padding: 2rem;
            gap: 2rem;
        }
        
        .main-content {
            flex: 3;
            min-width: 300px;
        }
        
        .sidebar {
            flex: 2;
            min-width: 280px;
        }
        
        .section {
            margin-bottom: 2.5rem;
        }
        
        .section-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 1.2rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--light-gray);
            display: flex;
            align-items: center;
        }
        
        .section-title i {
            margin-right: 10px;
        }
        
        /* Philosophy Section */
        .philosophy-card {
            background: var(--light);
            border-radius: var(--border-radius);
            padding: 1.8rem;
            box-shadow: var(--shadow);
            border-left: 4px solid var(--accent);
        }
        
        .philosophy-text {
            margin-bottom: 1.5rem;
            color: var(--secondary);
            font-size: 1.05rem;
        }
        
        .philosophy-points {
            list-style: none;
        }
        
        .philosophy-points li {
            margin-bottom: 1rem;
            padding-left: 1.8rem;
            position: relative;
        }
        
        .philosophy-points li i {
            position: absolute;
            left: 0;
            top: 0.2rem;
            color: var(--primary);
        }
        
        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
        }
        
        .tech-category {
            background: white;
            border-radius: var(--border-radius);
            padding: 1.2rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .tech-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .tech-category h4 {
            font-size: 1rem;
            margin-bottom: 0.8rem;
            color: var(--primary-dark);
            display: flex;
            align-items: center;
        }
        
        .tech-category h4 i {
            margin-right: 8px;
        }
        
        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        
        .tech-tag {
            background: var(--light-gray);
            color: var(--secondary);
            font-size: 0.8rem;
            padding: 0.3rem 0.7rem;
            border-radius: 4px;
            font-weight: 500;
        }
        
        /* Stats Section */
        .stats-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        
        .stat-card {
            flex: 1;
            min-width: 150px;
            background: white;
            border-radius: var(--border-radius);
            padding: 1.2rem;
            box-shadow: var(--shadow);
            text-align: center;
            transition: var(--transition);
        }
        
        .stat-card:hover {
            background: var(--light);
        }
        
        .stat-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.3rem;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: var(--gray);
            font-weight: 500;
        }
        
        /* Contact Section */
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }
        
        .contact-link {
            flex: 1;
            min-width: 120px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background: var(--light);
            color: var(--dark);
            text-decoration: none;
            padding: 0.9rem 1.2rem;
            border-radius: var(--border-radius);
            font-weight: 500;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }
        
        .contact-link:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-3px);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding: 2rem;
            background: var(--dark);
            color: white;
            margin-top: 2rem;
        }
        
        .footer-text {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .footer-subtext {
            opacity: 0.8;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .content {
                flex-direction: column;
                padding: 1.5rem;
            }
            
            .header {
                padding: 2rem 1rem;
            }
            
            .name-title {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .specialties {
                gap: 0.7rem;
            }
            
            .specialty {
                font-size: 0.85rem;
                padding: 0.4rem 0.9rem;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
            }
        }
        
        @media (max-width: 480px) {
            body {
                padding: 10px;
            }
            
            .header {
                padding: 1.5rem 1rem;
            }
            
            .name-title {
                font-size: 1.8rem;
            }
            
            .tagline {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.3rem;
            }
            
            .tech-grid {
                grid-template-columns: 1fr;
            }
            
            .stat-card {
                min-width: 100%;
            }
            
            .contact-link {
                min-width: 100%;
            }
        }
        
        /* Toggle for Tech Stack */
        .toggle-tech {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: var(--border-radius);
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            margin: 0 auto 1.5rem;
            transition: var(--transition);
        }
        
        .toggle-tech:hover {
            background: var(--primary-dark);
        }
        
        .full-tech-stack {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease;
        }
        
        .full-tech-stack.expanded {
            max-height: 2000px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <div class="profile-header">
                <h1 class="name-title">Eron Bruti</h1>
                <p class="tagline">Architecting Resilient Full-Stack Ecosystems</p>
                
                <div class="specialties">
                    <div class="specialty">System Architecture</div>
                    <div class="specialty">AI Solutions</div>
                    <div class="specialty">Full-Stack Development</div>
                    <div class="specialty">Cloud Infrastructure</div>
                </div>
            </div>
        </header>
        
        <!-- Main Content -->
        <div class="content">
            <main class="main-content">
                <!-- Philosophy Section -->
                <section class="section">
                    <h2 class="section-title"><i class="fas fa-compass"></i> My Philosophy</h2>
                    <div class="philosophy-card">
                        <p class="philosophy-text">
                            I engineer digital ecosystems. My work bridges deep back-end architecture with intelligent, human-centric user experiences. I don't just build applications; I design resilient, scalable platforms built for tomorrow's demands.
                        </p>
                        
                        <ul class="philosophy-points">
                            <li>
                                <i class="fas fa-brain"></i>
                                <strong>Systematic Design:</strong> Architecting secure, scalable, and AI-augmented platforms is the foundation of my work. Every great build starts with a clear blueprint.
                            </li>
                            <li>
                                <i class="fas fa-cogs"></i>
                                <strong>Full-Stack Execution:</strong> I command the entire technology stack, from optimizing Linux environments with <strong>Node.js</strong> to crafting intuitive front-ends with <strong>React</strong> and <strong>TypeScript</strong>.
                            </li>
                            <li>
                                <i class="fas fa-globe-europe"></i>
                                <strong>Local Impact, Global Standards:</strong> My mission is to elevate Kosovo's tech landscape by delivering software that competes on the world stage.
                            </li>
                        </ul>
                        
                        <p style="margin-top: 1.5rem; font-style: italic; color: var(--primary-dark);">
                            If you're building a purpose-driven platform, we should talk.
                        </p>
                    </div>
                </section>
                
                <!-- Tech Stack Section -->
                <section class="section">
                    <h2 class="section-title"><i class="fas fa-layer-group"></i> Core Tech Arsenal</h2>
                    
                    <div class="tech-grid">
                        <div class="tech-category">
                            <h4><i class="fas fa-code"></i> Languages</h4>
                            <div class="tech-tags">
                                <span class="tech-tag">TypeScript</span>
                                <span class="tech-tag">JavaScript</span>
                                <span class="tech-tag">GraphQL</span>
                                <span class="tech-tag">Python</span>
                            </div>
                        </div>
                        
                        <div class="tech-category">
                            <h4><i class="fas fa-desktop"></i> Frontend</h4>
                            <div class="tech-tags">
                                <span class="tech-tag">React</span>
                                <span class="tech-tag">Next.js</span>
                                <span class="tech-tag">Vue.js</span>
                                <span class="tech-tag">Tailwind</span>
                            </div>
                        </div>
                        
                        <div class="tech-category">
                            <h4><i class="fas fa-server"></i> Backend</h4>
                            <div class="tech-tags">
                                <span class="tech-tag">Node.js</span>
                                <span class="tech-tag">Express</span>
                                <span class="tech-tag">Socket.io</span>
                                <span class="tech-tag">JWT</span>
                            </div>
                        </div>
                        
                        <div class="tech-category">
                            <h4><i class="fas fa-database"></i> Databases</h4>
                            <div class="tech-tags">
                                <span class="tech-tag">PostgreSQL</span>
                                <span class="tech-tag">MySQL</span>
                                <span class="tech-tag">MongoDB</span>
                                <span class="tech-tag">Redis</span>
                            </div>
                        </div>
                        
                        <div class="tech-category">
                            <h4><i class="fas fa-cloud"></i> DevOps</h4>
                            <div class="tech-tags">
                                <span class="tech-tag">Docker</span>
                                <span class="tech-tag">Kubernetes</span>
                                <span class="tech-tag">AWS</span>
                                <span class="tech-tag">GitHub Actions</span>
                            </div>
                        </div>
                        
                        <div class="tech-category">
                            <h4><i class="fas fa-robot"></i> AI/ML</h4>
                            <div class="tech-tags">
                                <span class="tech-tag">TensorFlow</span>
                                <span class="tech-tag">PyTorch</span>
                                <span class="tech-tag">NVIDIA CUDA</span>
                                <span class="tech-tag">OpenAI</span>
                            </div>
                        </div>
                    </div>
                    
                    <button class="toggle-tech" id="toggleTechBtn">
                        <i class="fas fa-chevron-down"></i> View Full Tech Stack
                    </button>
                    
                    <div class="full-tech-stack" id="fullTechStack">
                        <!-- Expanded tech stack would go here -->
                        <div style="padding: 1.5rem; background: var(--light); border-radius: var(--border-radius);">
                            <p>Your full expanded tech stack with all badges would be displayed here in the full implementation.</p>
                            <p>This section would include all the technologies from your original README in an organized, responsive layout.</p>
                        </div>
                    </div>
                </section>
            </main>
            
            <!-- Sidebar -->
            <aside class="sidebar">
                <!-- Stats Section -->
                <section class="section">
                    <h2 class="section-title"><i class="fas fa-chart-line"></i> Development Metrics</h2>
                    
                    <div class="stats-container">
                        <div class="stat-card">
                            <div class="stat-value">1500+</div>
                            <div class="stat-label">Commits</div>
                        </div>
                        
                        <div class="stat-card">
                            <div class="stat-value">50+</div>
                            <div class="stat-label">Projects</div>
                        </div>
                        
                        <div class="stat-card">
                            <div class="stat-value">15+</div>
                            <div class="stat-label">Technologies</div>
                        </div>
                        
                        <div class="stat-card">
                            <div class="stat-value">5+</div>
                            <div class="stat-label">Years Experience</div>
                        </div>
                    </div>
                    
                    <div style="background: var(--light); border-radius: var(--border-radius); padding: 1.2rem; margin-bottom: 1.5rem;">
                        <h4 style="margin-bottom: 0.8rem; color: var(--primary-dark);">GitHub Activity</h4>
                        <p style="color: var(--gray); font-size: 0.95rem;">
                            Consistent contributor with a focus on open-source projects, system architecture, and AI research.
                        </p>
                    </div>
                </section>
                
                <!-- Contact Section -->
                <section class="section">
                    <h2 class="section-title"><i class="fas fa-network-wired"></i> Connect & Collaborate</h2>
                    
                    <p style="margin-bottom: 1.2rem; color: var(--secondary);">
                        I'm always open to connecting with fellow innovators and creators. Let's discuss system design, AI, or the future of tech.
                    </p>
                    
                    <div class="contact-links">
                        <a href="https://linkedin.com/in/eron-bruti-067b702aa" target="_blank" class="contact-link">
                            <i class="fab fa-linkedin"></i> LinkedIn
                        </a>
                        
                        <a href="mailto:brutieron@gmail.com" class="contact-link">
                            <i class="fas fa-envelope"></i> Email
                        </a>
                        
                        <a href="https://github.com/brutieron" target="_blank" class="contact-link">
                            <i class="fab fa-github"></i> GitHub
                        </a>
                        
                        <a href="https://instagram.com/brutieron" target="_blank" class="contact-link">
                            <i class="fab fa-instagram"></i> Instagram
                        </a>
                    </div>
                </section>
                
                <!-- Focus Areas -->
                <section class="section">
                    <h2 class="section-title"><i class="fas fa-bullseye"></i> Current Focus</h2>
                    
                    <div style="background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%); color: white; border-radius: var(--border-radius); padding: 1.5rem;">
                        <h4 style="margin-bottom: 0.8rem; font-size: 1.1rem;">AI-Augmented Platforms</h4>
                        <p style="font-size: 0.95rem; opacity: 0.9;">
                            Designing intelligent systems that leverage machine learning to create adaptive, human-centric user experiences.
                        </p>
                    </div>
                </section>
            </aside>
        </div>
        
        <!-- Footer -->
        <footer class="footer">
            <p class="footer-text">Architecting with Precision & Purpose</p>
            <p class="footer-subtext">Eron Bruti &copy; 2024 | Full-Stack Architect & AI Engineer</p>
        </footer>
    </div>

    <script>
        // Toggle expanded tech stack
        document.getElementById('toggleTechBtn').addEventListener('click', function() {
            const fullTechStack = document.getElementById('fullTechStack');
            const icon = this.querySelector('i');
            
            fullTechStack.classList.toggle('expanded');
            
            if (fullTechStack.classList.contains('expanded')) {
                this.innerHTML = '<i class="fas fa-chevron-up"></i> Collapse Tech Stack';
            } else {
                this.innerHTML = '<i class="fas fa-chevron-down"></i> View Full Tech Stack';
            }
        });
        
        // Add subtle animation to stat cards
        document.addEventListener('DOMContentLoaded', function() {
            const statCards = document.querySelectorAll('.stat-card');
            
            statCards.forEach((card, index) => {
                card.style.transitionDelay = `${index * 0.1}s`;
            });
        });
    </script>
</body>
</html>
