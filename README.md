# Muhammad_Umair.github.io

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jane Doe | AI Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6C63FF;
            --secondary: #4D44DB;
            --dark: #2F2E41;
            --light: #F9F9F9;
            --accent: #FF6584;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        /* Header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: var(--transition);
        }
        
        header.scrolled {
            padding: 1rem 5%;
            background-color: rgba(255, 255, 255, 0.98);
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 0.5rem;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2.5rem;
        }
        
        .nav-links a {
            font-weight: 500;
            position: relative;
            padding: 0.5rem 0;
            transition: var(--transition);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .nav-links a.active {
            color: var(--primary);
        }
        
        .menu-btn {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 5%;
            padding-top: 80px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: -50px;
            right: -50px;
            width: 600px;
            height: 600px;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            opacity: 0.1;
            z-index: 0;
        }
        
        .hero-content {
            max-width: 600px;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .hero h1 span {
            color: var(--primary);
        }
        
        .hero h2 {
            font-size: 1.5rem;
            font-weight: 400;
            margin-bottom: 1.5rem;
            color: #666;
        }
        
        .hero p {
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            background-color: var(--primary);
            color: white;
            border-radius: 50px;
            font-weight: 500;
            transition: var(--transition);
            border: 2px solid transparent;
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--primary);
            border-color: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(108, 99, 255, 0.2);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--primary);
            border-color: var(--primary);
            margin-left: 1rem;
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }
        
        .hero-image {
            position: absolute;
            right: 5%;
            bottom: 10%;
            width: 500px;
            z-index: 1;
        }
        
        .hero-image img {
            width: 100%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        
        .social-icons {
            display: flex;
            margin-top: 2rem;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--light);
            margin-right: 1rem;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }
        
        .social-icons a:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-3px);
        }
        
        /* About Section */
        .section {
            padding: 7rem 5%;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }
        
        .section-title p {
            color: #777;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding-right: 2rem;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
        }
        
        .about-text h3 span {
            color: var(--primary);
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            color: #555;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        .skill {
            background-color: white;
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
            font-size: 0.9rem;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .skill:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-3px);
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .about-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }
        
        /* Services Section */
        .services {
            background-color: #f9f9ff;
        }
        
        .services-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }
        
        .service-card {
            background-color: white;
            border-radius: 10px;
            padding: 2.5rem 2rem;
            flex: 1 1 300px;
            max-width: 350px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 100%;
            background-color: var(--primary);
            transition: var(--transition);
            z-index: -1;
            opacity: 0.1;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .service-card:hover::before {
            width: 100%;
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .service-card p {
            color: #666;
        }
        
        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .project-image {
            height: 200px;
            overflow: hidden;
        }
        
        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .project-card:hover .project-image img {
            transform: scale(1.1);
        }
        
        .project-info {
            padding: 1.5rem;
        }
        
        .project-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        
        .project-info p {
            color: #666;
            margin-bottom: 1rem;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }
        
        .project-tag {
            background-color: #eee;
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
        }
        
        .project-links {
            display: flex;
        }
        
        .project-links a {
            display: inline-block;
            padding: 0.5rem 1rem;
            background-color: var(--light);
            border-radius: 5px;
            margin-right: 1rem;
            font-size: 0.9rem;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .project-links a:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Contact Section */
        .contact {
            background-color: var(--dark);
            color: white;
        }
        
        .contact .section-title h2,
        .contact .section-title p {
            color: white;
        }
        
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-info p {
            opacity: 0.8;
            margin-bottom: 2rem;
        }
        
        .contact-details {
            margin-bottom: 2rem;
        }
        
        .contact-detail {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .contact-detail i {
            font-size: 1.5rem;
            margin-right: 1.5rem;
            color: var(--primary);
        }
        
        .contact-form {
            flex: 1;
            min-width: 300px;
            background-color: white;
            padding: 2.5rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(108, 99, 255, 0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            width: 100%;
            padding: 0.8rem 1rem;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .submit-btn:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(77, 68, 219, 0.3);
        }
        
        /* Footer */
        footer {
            background-color: #1a1a2e;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .footer-logo {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .footer-links {
            display: flex;
            list-style: none;
            margin-bottom: 1.5rem;
        }
        
        .footer-links li {
            margin: 0 1rem;
        }
        
        .footer-links a {
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: var(--primary);
        }
        
        .footer-social {
            display: flex;
            margin-bottom: 1.5rem;
        }
        
        .footer-social a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            margin: 0 0.5rem;
            transition: var(--transition);
        }
        
        .footer-social a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Animation Classes */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease-out;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-image {
                width: 400px;
            }
            
            .hero::before {
                width: 400px;
                height: 400px;
            }
        }
        
        @media (max-width: 768px) {
            .menu-btn {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                padding-top: 3rem;
                transition: var(--transition);
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 1rem 0;
            }
            
            header.scrolled .nav-links {
                top: 70px;
                height: calc(100vh - 70px);
            }
            
            .hero {
                flex-direction: column;
                text-align: center;
                padding-top: 100px;
                height: auto;
                padding-bottom: 3rem;
            }
            
            .hero-content {
                max-width: 100%;
                margin-bottom: 3rem;
            }
            
            .hero-btns {
                display: flex;
                flex-direction: column;
                gap: 1rem;
            }
            
            .btn-outline {
                margin-left: 0;
            }
            
            .hero-image {
                position: relative;
                right: auto;
                bottom: auto;
                width: 100%;
                max-width: 500px;
                margin: 0 auto;
            }
            
            .social-icons {
                justify-content: center;
            }
            
            .about-text {
                padding-right: 0;
                margin-bottom: 3rem;
            }
            
            .about-image {
                order: -1;
            }
            
            .project-card {
                max-width: 100%;
            }
        }
        
        @media (max-width: 576px) {
            .section {
                padding: 5rem 2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero h2 {
                font-size: 1.2rem;
            }
            
            .hero::before {
                width: 300px;
                height: 300px;
                top: -30px;
                right: -30px;
            }
            
            .hero-image {
                max-width: 300px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <a href="#" class="logo"><i class="fas fa-robot"></i> Jane Doe</a>
        <div class="menu-btn">
            <i class="fas fa-bars"></i>
        </div>
        <ul class="nav-links">
            <li><a href="#home" class="active">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content fade-in">
            <h1>Hi, I'm <span>Jane Doe</span></h1>
            <h2>AI & Machine Learning Engineer</h2>
            <p>I design and implement cutting-edge AI solutions to solve complex problems. With expertise in deep learning, computer vision, and natural language processing, I bridge the gap between research and real-world applications.</p>
            <div class="hero-btns">
                <a href="#projects" class="btn">View My Work</a>
                <a href="#contact" class="btn btn-outline">Hire Me</a>
            </div>
            <div class="social-icons">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-kaggle"></i></a>
                <a href="#"><i class="fas fa-file-pdf"></i></a>
            </div>
        </div>
        <div class="hero-image">
            <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="AI Illustration">
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="section-title">
            <h2>About Me</h2>
            <p>Learn more about my background, skills, and professional journey</p>
        </div>
        <div class="about-content">
            <div class="about-text fade-in">
                <h3>Who am <span>I?</span></h3>
                <p>I'm an AI Engineer with 5+ years of experience specializing in machine learning and deep learning applications. I hold a Master's degree in Computer Science with a focus on Artificial Intelligence from Stanford University.</p>
                <p>My professional journey includes working with tech startups and Fortune 500 companies to implement AI solutions that drive business value. I'm passionate about creating intelligent systems that improve lives and transform industries.</p>
                <p>When I'm not coding, you can find me contributing to open-source AI projects, mentoring aspiring data scientists, or exploring the latest research papers in machine learning.</p>
                
                <h3>My <span>Skills</span></h3>
                <div class="skills">
                    <span class="skill">Python</span>
                    <span class="skill">TensorFlow</span>
                    <span class="skill">PyTorch</span>
                    <span class="skill">Keras</span>
                    <span class="skill">Computer Vision</span>
                    <span class="skill">NLP</span>
                    <span class="skill">Deep Learning</span>
                    <span class="skill">Neural Networks</span>
                    <span class="skill">Data Science</span>
                    <span class="skill">Big Data</span>
                    <span class="skill">Cloud AI</span>
                    <span class="skill">MLOps</span>
                </div>
            </div>
            <div class="about-image fade-in">
                <img src="https://images.unsplash.com/photo-1596495577886-d920f1fb7238?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80" alt="About Me">
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="section services" id="services">
        <div class="section-title">
            <h2>My Services</h2>
            <p>Here are some of the AI and machine learning services I provide</p>
        </div>
        <div class="services-container">
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-brain"></i>
                </div>
                <h3>Machine Learning</h3>
                <p>Design and implementation of predictive models, recommendation systems, and classification algorithms tailored to your business needs.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-eye"></i>
                </div>
                <h3>Computer Vision</h3>
                <p>Development of image and video analysis solutions including object detection, facial recognition, and medical imaging diagnostics.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-language"></i>
                </div>
                <h3>Natural Language Processing</h3>
                <p>Building chatbots, sentiment analysis systems, text summarization, and other language understanding applications.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-chart-line"></i>
                </div>
                <h3>Data Science</h3>
                <p>Extracting insights from complex datasets, creating visualizations, and developing data-driven decision-making tools.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-server"></i>
                </div>
                <h3>AI Integration</h3>
                <p>Deploying trained models into production environments with API development, cloud deployment, and system integration.</p>
            </div>
            
            <div class="service-card fade-in">
                <div class="service-icon">
                    <i class="fas fa-graduation-cap"></i>
                </div>
                <h3>AI Training</h3>
                <p>Conducting workshops and training sessions to upskill your team in AI fundamentals and practical applications.</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="section" id="projects">
        <div class="section-title">
            <h2>My Projects</h2>
            <p>Some of my recent AI and machine learning projects</p>
        </div>
        <div class="projects-container">
            <div class="project-card fade-in">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1655720828013-1c8dc93420d3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Medical Diagnosis AI">
                </div>
                <div class="project-info">
                    <h3>Medical Diagnosis AI</h3>
                    <p>Deep learning system that analyzes medical images with 98% accuracy in detecting early signs of diseases.</p>
                    <div class="project-tags">
                        <span class="project-tag">Python</span>
                        <span class="project-tag">TensorFlow</span>
                        <span class="project-tag">Computer Vision</span>
                        <span class="project-tag">Healthcare</span>
                    </div>
                    <div class="project-links">
                        <a href="#"><i class="fab fa-github"></i> Code</a>
                        <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                    </div>
                </div>
            </div>
            
            <div class="project-card fade-in">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80" alt="Smart Chatbot">
                </div>
                <div class="project-info">
                    <h3>Enterprise Chatbot</h3>
                    <p>Conversational AI assistant that handles customer inquiries with natural language understanding and context awareness.</p>
                    <div class="project-tags">
                        <span class="project-tag">NLP</span>
                        <span class="project-tag">Transformers</span>
                        <span class="project-tag">BERT</span>
                        <span class="project-tag">Customer Service</span>
                    </div>
                    <div class="project-links">
                        <a href="#"><i class="fab fa-github"></i> Code</a>
                        <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                    </div>
                </div>
            </div>
            
            <div class="project-card fade-in">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1610563166150-b34df4f3bcd6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80" alt="Autonomous Vehicles">
                </div>
                <div class="project-info">
                    <h3>Autonomous Vehicle Perception</h3>
                    <p>Real-time object detection and tracking system for self-driving cars using deep neural networks.</p>
                    <div class="project-tags">
                        <span class="project-tag">PyTorch</span>
                        <span class="project-tag">YOLO</span>
                        <span class="project-tag">Reinforcement Learning</span>
                        <span class="project-tag">Robotics</span>
                    </div>
                    <div class="project-links">
                        <a href="#"><i class="fab fa-github"></i> Code</a>
                        <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                    </div>
                </div>
            </div>
            
            <div class="project-card fade-in">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1605371924599-2d0365da1ae0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1374&q=80" alt="Fraud Detection">
                </div>
                <div class="project-info">
                    <h3>Financial Fraud Detection</h3>
                    <p>Anomaly detection system that identifies fraudulent transactions with 99.7% accuracy using ensemble learning.</p>
                    <div class="project-tags">
                        <span class="project-tag">Scikit-learn</span>
                        <span class="project-tag">XGBoost</span>
                        <span class="project-tag">Anomaly Detection</span>
                        <span class="project-tag">Finance</span>
                    </div>
                    <div class="project-links">
                        <a href="#"><i class="fab fa-github"></i> Code</a>
                        <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                    </div>
                </div>
            </div>
            
            <div class="project-card fade-in">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1620712943543-bcc4688e7485?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1365&q=80" alt="Stock Market Prediction">
                </div>
                <div class="project-info">
                    <h3>Stock Market Predictor</h3>
                    <p>Time series forecasting model that predicts stock prices using LSTM networks and sentiment analysis.</p>
                    <div class="project-tags">
                        <span class="project-tag">LSTM</span>
                        <span class="project-tag">Sentiment Analysis</span>
                        <span class="project-tag">Finance</span>
                        <span class="project-tag">Trading</span>
                    </div>
                    <div class="project-links">
                        <a href="#"><i class="fab fa-github"></i> Code</a>
                        <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                    </div>
                </div>
            </div>
            
            <div class="project-card fade-in">
                <div class="project-image">
                    <img src="https://images.unsplash.com/photo-1664478546384-d1ffe1aff6d9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D3D&auto=format&fit=crop&w=1364&q=80" alt="AI Content Generator">
                </div>
                <div class="project-info">
                    <h3>AI Content Generator</h3>
                    <p>GPT-based model that creates marketing content, blog posts, and social media copy tailored to brand voice.</p>
                    <div class="project-tags">
                        <span class="project-tag">GPT-3</span>
                        <span class="project-tag">Transformers</span>
                        <span class="project-tag">Content Generation</span>
                        <span class="project-tag">Marketing</span>
                    </div>
                    <div class="project-links">
                        <a href="#"><i class="fab fa-github"></i> Code</a>
                        <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact" id="contact">
        <div class="section-title">
            <h2>Get In Touch</h2>
            <p>Have a project in mind or want to discuss potential collaboration? I'd love to hear from you!</p>
        </div>
        <div class="contact-container">
            <div class="contact-info fade-in">
                <h3>Let's Connect</h3>
                <p>I'm currently available for freelance work, consulting, or full-time positions. If you have any questions or just want to say hi, feel free to reach out.</p>
                
                <div class="contact-details">
                    <div class="contact-detail">
                        <i class="fas fa-envelope"></i>
                        <div>
                            <h4>Email</h4>
                            <p>jane.doe@aiengineer.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-detail">
                        <i class="fas fa-phone-alt"></i>
                        <div>
                            <h4>Phone</h4>
                            <p>+1 (555) 123-4567</p>
                        </div>
                    </div>
                    
                    <div class="contact-detail">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Location</h4>
                            <p>San Francisco, CA</p>
                        </div>
                    </div>
                </div>
                
                <div class="social-icons">
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-kaggle"></i></a>
                    <a href="#"><i class="fas fa-file-pdf"></i></a>
                </div>
            </div>
            
            <div class="contact-form fade-in">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" class="form-control" id="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" class="form-control" id="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" class="form-control" id="subject">
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea class="form-control" id="message" rows="5" required></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <a href="#" class="footer-logo"><i class="fas fa-robot"></i> Jane Doe</a>
            <ul class="footer-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="footer-social">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-kaggle"></i></a>
            </div>
            <p class="copyright">© 2023 Jane Doe. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const menuBtn = document.querySelector('.menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        menuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            menuBtn.innerHTML = navLinks.classList.contains('active') ? 
                '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
        });
        
        // Sticky Header
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            header.classList.toggle('scrolled', window.scrollY > 0);
        });
        
        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                if(navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                    menuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                }
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
                
                // Update active nav link
                document.querySelectorAll('.nav-links a').forEach(link => {
                    link.classList.remove('active');
                });
                this.classList.add('active');
            });
        });
        
        // Form Submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // Here you would typically send the form data to a server
            console.log({ name, email, subject, message });
            
            // Show success message
            alert('Thank you for your message! I will get back to you soon.');
            
            // Reset form
            this.reset();
        });
        
        // Scroll Reveal Animation
        const fadeElements = document.querySelectorAll('.fade-in');
        
        const fadeInOnScroll = () => {
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if(elementTop < windowHeight - 100) {
                    element.classList.add('visible');
                }
            });
        };
        
        // Initial check
        fadeInOnScroll();
        
        // Check on scroll
        window.addEventListener('scroll', fadeInOnScroll);
    </script>
</body>
</html>
