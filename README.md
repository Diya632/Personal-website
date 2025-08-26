# Personal-website
file:///C:/Users/dell/Documents/Personal%20website/Pesonal%20website.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diya - Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #FF6B6B;
            --secondary: #4ECDC4;
            --dark: #36292e;
            --light: #F7FFF7;
            --accent: #FFE66D;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
            padding: 6rem 2rem;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
            margin-bottom: 4rem;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 600;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            margin: 0 auto 1.5rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        section {
            padding: 4rem 0;
            border-bottom: 1px solid rgba(0,0,0,0.1);
        }
        
        section:last-child {
            border-bottom: none;
        }
        
        h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 50px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
            align-items: center;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .skill {
            background-color: var(--secondary);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .project-info {
            padding: 1.5rem;
        }
        
        .project-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }
        
        .contact-form {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.5rem;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        label {
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        input, textarea {
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: inherit;
            font-size: 1rem;
        }
        
        textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        button {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 1rem 2rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        button:hover {
            background-color: #e05555;
        }
        
        footer {
            text-align: center;
            padding: 2rem;
            background-color: var(--dark);
            color: white;
            margin-top: 4rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1rem;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255,255,255,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }
        
        .social-icon:hover {
            background-color: var(--primary);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
        }
        
        /* Floating animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://placehold.co/400x400" alt="Diya, a smiling young woman with wavy hair wearing professional attire" class="profile-image floating">
        <h1>Diya</h1>
        <p class="tagline">Creative Professional & Problem Solver</p>
        <a href="#contact" class="btn">Get In Touch</a>
    </header>
    
    <main class="container">
        <section id="about">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Hello! I'm Diya, a student currently studying Bachelor's of Computer Application . I believe in combining creativity with analytical thinking to solve complex problems and create beautiful solutions.</p>
                    <p> I am a young energetic girl currently studying at last year.With all the years of these educational institutions ,I 
                        learnt to boost my self confidence and interpersonal skills. This is my personal website I have created with skills.
                    </p>
                    
                    <h3 style="margin-top: 1.5rem;">Skills & Expertise</h3>
                    <div class="skills">
                        <span class="skill">Web Designing</span>
                        <span class="skill">Digital Marketing</span>
                        <span class="skill">JavaScript</span>
                        <span class="skill">Problem Solving</span>
                        <span class="skill">Mern Stack Development</span>
                        <span class="skill">Mobile App Development</span>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://placehold.co/500x600" alt="Diya working at a modern workstation with multiple screens and creative tools" style="max-width: 100%; border-radius: 8px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
                </div>
            </div>
        </section>
        
        
                    </div>
                </div>
                
                
                    </div>
                </div>
            </div>
        </section>
        
        <section id="contact">
            
            <h2>Let's Connect</h2>
            <p>Have a project in mind or want to discuss opportunities? I'd love to hear from you!</p>
            
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject">
                </div>
                
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                
                <button type="submit">Send Message</button>
            </form>
        </section>
    </main>
    
    <footer>
        <p>&copy; <span id="year"></span> Diya. All rights reserved.</p>
        <div class="social-links">
            <a href="#" class="social-icon">Li</a>
            <a href="#" class="social-icon">Tw</a>
            <a href="#" class="social-icon">In</a>
            <a href="#" class="social-icon">Gh</a>
        </div>
    </footer>
    
    <script>
        // Update copyright year automatically
        document.getElementById('year').textContent = new Date().getFullYear();
        
        // Form submission handling
        const form = document.querySelector('.contact-form');
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // Here you would typically send the data to a server
            // For now, we'll just log it and show an alert
            console.log({name, email, subject, message});
            
            alert(`Thank you for your message, ${name}! I'll get back to you soon.`);
            form.reset();
        });
        
        // Animate elements when they come into view
        const observerOptions = {
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
