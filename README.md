# Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Sneha Meshram | Executive Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: radial-gradient(circle at top left, rgba(30, 74, 147, 0.24), transparent 25%),
                radial-gradient(circle at 80% 20%, rgba(31, 115, 255, 0.16), transparent 20%),
                linear-gradient(180deg, #03111f 0%, #020a18 100%);
    color: #E8F4FF;
    line-height: 1.6;
    overflow-x: hidden;
}

/* NAVIGATION */
nav {
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
    padding: 2rem 4rem;
    background: rgba(0, 0, 0, 0.8);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.nav-container {
    max-width: 1400px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    font-weight: 600;
    color: #FFFFFF;
    letter-spacing: -0.02em;
}

.nav-links {
    display: flex;
    gap: 3rem;
}

.nav-links a {
    color: rgba(255, 255, 255, 0.8);
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    transition: all 0.3s ease;
    position: relative;
}

.nav-links a:hover {
    color: #7CC7FF;
}

.nav-links a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background: #7CC7FF;
    transition: width 0.3s ease;
}

.nav-links a:hover::after {
    width: 100%;
}

/* HERO SECTION */
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
}

.hero-container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 4rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.hero-content {
    z-index: 2;
}

.hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 8vw, 5rem);
    font-weight: 600;
    color: #FFFFFF;
    line-height: 1.1;
    margin-bottom: 1.5rem;
    letter-spacing: -0.02em;
}

.hero-subtitle {
    font-size: 1.3rem;
    color: rgba(255, 255, 255, 0.8);
    margin-bottom: 2rem;
    font-weight: 400;
    max-width: 500px;
}

.hero-cta {
    display: inline-flex;
    align-items: center;
    gap: 1rem;
    background: linear-gradient(135deg, #4FA9FF, #1B6DFF);
    color: #FFFFFF;
    padding: 1rem 2rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
    transition: all 0.3s ease;
    box-shadow: 0 16px 40px rgba(28, 110, 255, 0.25);
}

.hero-cta:hover {
    transform: translateY(-2px);
    box-shadow: 0 18px 50px rgba(28, 110, 255, 0.3);
}


.hero-image {
    position: relative;
    z-index: 2;
}

.hero-image img {
    width: 100%;
    max-width: 500px;
    height: auto;
    border-radius: 20px;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
}

/* BACKGROUND ELEMENTS */
.hero-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle at 25% 20%, rgba(95, 174, 255, 0.18), transparent 28%),
                radial-gradient(circle at 80% 25%, rgba(23, 122, 255, 0.12), transparent 18%),
                radial-gradient(circle at 50% 80%, rgba(8, 44, 102, 0.9), transparent 50%);
    z-index: 1;
    overflow: hidden;
}

.hero-bg::before,
.hero-bg::after {
    content: '';
    position: absolute;
    border-radius: 50%;
    filter: blur(60px);
    opacity: 0.65;
    animation: floatBg 18s ease-in-out infinite;
}

.hero-bg::before {
    width: 360px;
    height: 360px;
    top: 10%;
    left: 10%;
    background: rgba(92, 178, 255, 0.22);
}

.hero-bg::after {
    width: 260px;
    height: 260px;
    bottom: 10%;
    right: 15%;
    background: rgba(23, 105, 255, 0.18);
    animation-duration: 22s;
}

@keyframes floatBg {
    0% {
        transform: translate(0, 0) scale(1);
    }
    50% {
        transform: translate(30px, -20px) scale(1.05);
    }
    100% {
        transform: translate(0, 0) scale(1);
    }
}

.hero-3d {
    position: absolute;
    top: 50%;
    right: 8%;
    width: 280px;
    height: 280px;
    z-index: 1;
    perspective: 1200px;
}

.hero-3d-inner {
    position: relative;
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    animation: rotate3d 18s linear infinite;
}

.hero-3d-ring,
.hero-3d-core {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
}

.hero-3d-ring {
    width: 100%;
    height: 100%;
    border: 2px solid rgba(127, 206, 255, 0.18);
    box-shadow: 0 0 40px rgba(79, 169, 255, 0.2);
    transform: rotateX(70deg);
}

.hero-3d-core {
    width: 140px;
    height: 140px;
    background: radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.95), rgba(79, 169, 255, 0.35) 45%, transparent 80%);
    box-shadow: 0 0 80px rgba(79, 169, 255, 0.45);
}

.hero-image {
    position: relative;
    z-index: 2;
    perspective: 1000px;
}

.hero-image img {
    width: 100%;
    max-width: 500px;
    height: auto;
    border-radius: 20px;
    box-shadow: 0 20px 80px rgba(0, 0, 0, 0.5);
    transform: translateZ(30px);
    transition: transform 0.4s ease;
}

.hero-image:hover img {
    transform: translateZ(40px) scale(1.02);
}

@keyframes rotate3d {
    0% {
        transform: rotateX(15deg) rotateY(0deg);
    }
    100% {
        transform: rotateX(15deg) rotateY(360deg);
    }
}

/* SECTIONS */
.section {
    padding: 8rem 4rem;
    max-width: 1400px;
    margin: 0 auto;
}

.section-title {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 600;
    color: #FFFFFF;
    text-align: center;
    margin-bottom: 4rem;
    position: relative;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
    background: #FFD700;
    border-radius: 2px;
}

/* CARDS */
.card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 2rem;
    margin-top: 3rem;
}

.card {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 20px;
    padding: 2.5rem;
    transition: all 0.4s ease;
    position: relative;
    overflow: hidden;
}

.card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(90deg, #FFD700, transparent);
    opacity: 0;
    transition: opacity 0.3s ease;
}

.card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 60px rgba(255, 215, 0, 0.15);
    border-color: rgba(255, 215, 0, 0.3);
}

.card:hover::before {
    opacity: 1;
}

.card-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    font-weight: 600;
    color: #FFD700;
    margin-bottom: 1rem;
}

.card-text {
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.7;
}

/* SKILLS SECTION */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
    margin-top: 3rem;
}

.skill-card {
    background: rgba(255, 255, 255, 0.03);
    backdrop-filter: blur(15px);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    padding: 2rem;
    text-align: center;
    transition: all 0.3s ease;
}

.skill-card:hover {
    background: rgba(255, 255, 255, 0.08);
    transform: translateY(-4px);
}

.skill-name {
    font-size: 1.2rem;
    font-weight: 600;
    color: #FFFFFF;
    margin-bottom: 1rem;
}

.skill-description {
    color: rgba(255, 255, 255, 0.7);
    font-size: 0.9rem;
    margin-bottom: 1.5rem;
}

.skill-bar {
    width: 100%;
    height: 4px;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 2px;
    overflow: hidden;
    margin-bottom: 0.5rem;
}

.skill-fill {
    height: 100%;
    background: linear-gradient(90deg, #FFD700, #FFA500);
    border-radius: 2px;
    transition: width 1.5s ease;
}

.skill-percentage {
    font-size: 0.8rem;
    color: rgba(255, 255, 255, 0.6);
    font-weight: 500;
}

/* TIMELINE */
.timeline {
    position: relative;
    max-width: 800px;
    margin: 3rem auto 0;
    padding-left: 2rem;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 24px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: linear-gradient(180deg, rgba(255, 215, 0, 0.9), rgba(255, 215, 0, 0.15));
}

.timeline-item {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(15px);
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 20px;
    padding: 2rem;
    margin-bottom: 2rem;
    position: relative;
    transition: all 0.3s ease;
}

.timeline-item::before {
    left: -32px;
}

.timeline-item:hover {
    background: rgba(255, 255, 255, 0.08);
    transform: translateX(10px);
}

.timeline-item::before {
    content: '';
    position: absolute;
    left: -15px;
    top: 2rem;
    width: 8px;
    height: 8px;
    background: #FFD700;
    border-radius: 50%;
    box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
}

.timeline-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    font-weight: 600;
    color: #FFD700;
    margin-bottom: 0.5rem;
}

.timeline-subtitle {
    color: rgba(255, 255, 255, 0.8);
    font-weight: 500;
    margin-bottom: 1rem;
}

.timeline-text {
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.6;
}

/* CONTACT FORM */
.contact-form {
    max-width: 600px;
    margin: 3rem auto 0;
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-input {
    width: 100%;
    padding: 1rem 1.5rem;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 12px;
    color: #FFFFFF;
    font-family: 'Inter', sans-serif;
    font-size: 1rem;
    transition: all 0.3s ease;
}

.form-input:focus {
    outline: none;
    border-color: #FFD700;
    box-shadow: 0 0 20px rgba(255, 215, 0, 0.2);
}

.form-input::placeholder {
    color: rgba(255, 255, 255, 0.5);
}

.form-textarea {
    min-height: 120px;
    resize: vertical;
}

.form-submit {
    width: 100%;
    padding: 1rem 2rem;
    background: linear-gradient(135deg, #FFD700, #FFA500);
    color: #000000;
    border: none;
    border-radius: 50px;
    font-weight: 600;
    font-size: 1rem;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 8px 32px rgba(255, 215, 0, 0.3);
}

.form-submit:hover {
    transform: translateY(-2px);
    box-shadow: 0 12px 40px rgba(255, 215, 0, 0.4);
}

/* FOOTER */
footer {
    background: rgba(255, 255, 255, 0.02);
    backdrop-filter: blur(20px);
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    padding: 3rem 4rem;
    text-align: center;
}

.footer-content {
    max-width: 1400px;
    margin: 0 auto;
}

.footer-text {
    color: rgba(255, 255, 255, 0.7);
    font-size: 0.9rem;
    margin-bottom: 2rem;
}

.social-links {
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.social-link {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50px;
    height: 50px;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    color: rgba(255, 255, 255, 0.8);
    text-decoration: none;
    font-size: 1.2rem;
    transition: all 0.3s ease;
}

.social-link:hover {
    background: rgba(255, 215, 0, 0.1);
    border-color: #FFD700;
    color: #FFD700;
    transform: translateY(-2px);
}

/* ANIMATIONS */
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
    animation: fadeInUp 0.8s ease forwards;
}

/* RESPONSIVE DESIGN */
@media (max-width: 1024px) {
    .hero-container {
        grid-template-columns: 1fr;
        gap: 3rem;
        text-align: center;
    }

    .nav-links {
        gap: 2rem;
    }

    .section {
        padding: 6rem 2rem;
    }
}

@media (max-width: 768px) {
    nav {
        padding: 1.5rem 2rem;
    }

    .nav-links {
        display: none;
    }

    .hero-container {
        padding: 0 2rem;
    }

    .hero-title {
        font-size: clamp(2.5rem, 10vw, 4rem);
    }

    .section {
        padding: 4rem 2rem;
    }

    .card-grid {
        grid-template-columns: 1fr;
    }

    .skills-grid {
        grid-template-columns: 1fr;
    }
}

</style>
</head>

<body>

<!-- NAVIGATION -->
<nav>
    <div class="nav-container">
        <div class="logo">Sneha Meshram</div>
        <div class="nav-links">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#academics">Academics</a>
            <a href="#skills">Skills</a>
            <a href="#projects">Projects</a>
            <a href="#achievements">Achievements</a>
            <a href="#contact">Contact</a>
        </div>
    </div>
</nav>

<!-- HERO SECTION -->
<div id="home" class="hero">
    <div class="hero-bg"></div>
    <div class="hero-3d">
        <div class="hero-3d-inner">
            <div class="hero-3d-ring"></div>
            <div class="hero-3d-core"></div>
        </div>
    </div>
    <div class="hero-container">
        <div class="hero-content">
            <h1 class="hero-title">Sneha Meshram</h1>
            <p class="hero-subtitle">Technology Executive & Computer Engineering Leader</p>
            <div id="typing" style="font-style: italic; color: rgba(255,255,255,0.8); margin-bottom: 2rem;"></div>
            <a href="#contact" class="hero-cta">
                Connect With Me
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7 17L17 7M17 7H7M17 7V17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </a>
        </div>
        <div class="hero-image">
            <img src="C:\Users\LENOVO\Downloads\Portfolio\Portfolio Photo.jpeg" alt="Sneha Meshram - Technology Executive">
        </div>
    </div>
</div>

<!-- ABOUT -->
<section id="about" class="section">
    <h2 class="section-title">About Me</h2>
    <div class="card">
        <p class="card-text">
            I am a dedicated Computer Engineering professional with a relentless pursuit of excellence in technology and innovation. My journey began with a deep curiosity about how technology shapes our world, evolving into a comprehensive skill set that spans programming, system design, and strategic problem-solving.
        </p>
        <p class="card-text">
            Currently pursuing my B.Tech at MIT AOE Pune, I have demonstrated exceptional academic performance while actively engaging in cutting-edge projects and continuous professional development. My approach combines technical expertise with business acumen, preparing me for leadership roles in the rapidly evolving tech landscape.
        </p>
    </div>
</section>

<!-- ACADEMICS -->
<section id="academics" class="section">
    <h2 class="section-title">Academic Excellence</h2>
    <div class="timeline">
        <div class="timeline-item">
            <h3 class="timeline-title">B.Tech Computer Engineering</h3>
            <p class="timeline-subtitle">MIT Academy of Engineering, Pune (2025–Present)</p>
            <p class="timeline-text">Currently pursuing advanced coursework in computer engineering, focusing on software development, algorithms, data structures, and system design. Maintaining exceptional academic standing while engaging in practical projects and research initiatives.</p>
        </div>
        <div class="timeline-item">
            <h3 class="timeline-title">Higher Secondary Certificate</h3>
            <p class="timeline-subtitle">JNV (2024–25) - 75%</p>
            <p class="timeline-text">Achieved strong performance in Science stream, demonstrating solid foundation in mathematics, physics, and chemistry. Excelled in competitive examinations and developed analytical thinking skills.</p>
        </div>
        <div class="timeline-item">
            <h3 class="timeline-title">Secondary School Certificate</h3>
            <p class="timeline-subtitle">JNV (2022–23) - 80%</p>
            <p class="timeline-text">Secured outstanding results, establishing a strong academic foundation. Recognized for exceptional performance in science and mathematics, laying the groundwork for engineering excellence.</p>
        </div>
    </div>
</section>

<!-- SKILLS -->
<section id="skills" class="section">
    <h2 class="section-title">Technical Expertise</h2>
    <div class="skills-grid">
        <div class="skill-card">
            <h4 class="skill-name">C Programming</h4>
            <p class="skill-description">Advanced proficiency in system-level programming, memory management, and algorithm implementation.</p>
            <div class="skill-bar">
                <div class="skill-fill" style="width: 75%;"></div>
            </div>
            <div class="skill-percentage">75%</div>
        </div>
        <div class="skill-card">
            <h4 class="skill-name">Python Development</h4>
            <p class="skill-description">Strong command of Python for data analysis, automation, and application development.</p>
            <div class="skill-bar">
                <div class="skill-fill" style="width: 60%;"></div>
            </div>
            <div class="skill-percentage">60%</div>
        </div>
        <div class="skill-card">
            <h4 class="skill-name">Linux Systems</h4>
            <p class="skill-description">Expertise in Linux environment, command-line operations, and system administration.</p>
            <div class="skill-bar">
                <div class="skill-fill" style="width: 70%;"></div>
            </div>
            <div class="skill-percentage">70%</div>
        </div>
        <div class="skill-card">
            <h4 class="skill-name">Networking Fundamentals</h4>
            <p class="skill-description">Solid understanding of network protocols, Cisco technologies, and infrastructure design.</p>
            <div class="skill-bar">
                <div class="skill-fill" style="width: 80%;"></div>
            </div>
            <div class="skill-percentage">80%</div>
        </div>
        <div class="skill-card">
            <h4 class="skill-name">Problem Solving</h4>
            <p class="skill-description">Exceptional analytical and logical reasoning skills for complex technical challenges.</p>
            <div class="skill-bar">
                <div class="skill-fill" style="width: 85%;"></div>
            </div>
            <div class="skill-percentage">85%</div>
        </div>
        <div class="skill-card">
            <h4 class="skill-name">Leadership</h4>
            <p class="skill-description">Proven ability to lead teams, manage projects, and drive strategic initiatives.</p>
            <div class="skill-bar">
                <div class="skill-fill" style="width: 90%;"></div>
            </div>
            <div class="skill-percentage">90%</div>
        </div>
    </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="section">
    <h2 class="section-title">Strategic Initiatives & Projects</h2>
    <div class="card-grid">
        <div class="card">
            <h3 class="card-title">Advanced Calculator Application</h3>
            <p class="card-text">Led the development of a comprehensive calculator application in C, implementing complex arithmetic operations and user interface design. This project enhanced my understanding of algorithmic efficiency and user experience principles, resulting in a robust tool for mathematical computations.</p>
        </div>
        <div class="card">
            <h3 class="card-title">Student Information Management System</h3>
            <p class="card-text">Architected and implemented a sophisticated database management system for student records, incorporating advanced file handling techniques and data structures. The system provides efficient data retrieval and management capabilities, demonstrating enterprise-level programming skills.</p>
        </div>
        <div class="card">
            <h3 class="card-title">Linux System Administration Project</h3>
            <p class="card-text">Executed a comprehensive Linux-based project focusing on system optimization and automation. Implemented advanced command-line operations and shell scripting, resulting in improved system performance and operational efficiency.</p>
        </div>
        <div class="card">
            <h3 class="card-title">Collaborative Content Platform</h3>
            <p class="card-text">Spearheaded a team-based initiative to develop a podcast community platform, emphasizing cross-functional collaboration and content management. This project honed my leadership skills and ability to coordinate diverse teams toward common objectives.</p>
        </div>
    </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements" class="section">
    <h2 class="section-title">Certifications & Achievements</h2>
    <div class="card-grid">
        <div class="card">
            <h3 class="card-title">Cisco Python Essentials 1 & 2</h3>
            <p class="card-text">Successfully completed comprehensive Python programming courses, mastering fundamental and advanced concepts. Achieved 100% completion with distinction, demonstrating proficiency in Python development and problem-solving methodologies.</p>
        </div>
        <div class="card">
            <h3 class="card-title">NASSCOM Digital Skills Certification</h3>
            <p class="card-text">Completed an intensive 30-hour digital skills program covering industry-relevant technologies and best practices. This certification validates expertise in digital transformation and modern workplace competencies.</p>
        </div>
        <div class="card">
            <h3 class="card-title">Cisco Networking Fundamentals</h3>
            <p class="card-text">Achieved 100% completion in Cisco Networking Basics course, gaining deep insights into network architecture, protocols, and infrastructure design. Prepared for advanced networking certifications and enterprise network management.</p>
        </div>
        <div class="card">
            <h3 class="card-title">Academic Excellence Recognition</h3>
            <p class="card-text">Consistently maintained top academic performance with 80% in SSC and 75% in HSC examinations. Recognized for outstanding achievements in science and mathematics, establishing a strong foundation for engineering excellence.</p>
        </div>
    </div>
</section>

<!-- CONTACT -->
<section id="contact" class="section">
    <h2 class="section-title">Let’s Connect</h2>
    <div class="card">
        <p class="card-text">For business inquiries, collaboration opportunities, or professional discussions, please reach out using the form below. I am always interested in connecting with industry leaders, potential mentors, and innovative projects.</p>
    </div>
    <form class="contact-form">
        <div class="form-group">
            <input type="text" class="form-input" placeholder="Your Name" required>
        </div>
        <div class="form-group">
            <input type="email" class="form-input" placeholder="Your Email" required>
        </div>
        <div class="form-group">
            <textarea class="form-input form-textarea" placeholder="Your Message" required></textarea>
        </div>
        <button type="submit" class="form-submit">Send Message</button>
    </form>
</section>

<!-- FOOTER -->
<footer>
    <div class="footer-content">
        <p class="footer-text">&copy; 2024 Sneha Meshram. All rights reserved. | Aspiring Technology Executive & Computer Engineering Leader</p>
        <div class="social-links">
            <a href="#" class="social-link" title="LinkedIn">💼</a>
            <a href="#" class="social-link" title="GitHub">💻</a>
            <a href="#" class="social-link" title="Email">📧</a>
            <a href="#" class="social-link" title="Twitter">🐦</a>
        </div>
    </div>
</footer>

<script>

// Intersection Observer for scroll animations
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
    
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('fade-in');
        }
    });
}, observerOptions);

// Observe all sections
document.querySelectorAll('section').forEach(section => {
    observer.observe(section);
});

// Observe cards
document.querySelectorAll('.card').forEach(card => {
    observer.observe(card);
});

// Observe skill cards
document.querySelectorAll('.skill-card').forEach(card => {
    observer.observe(card);
});

// Observe timeline items
document.querySelectorAll('.timeline-item').forEach(item => {
    observer.observe(item);
});

// Smooth scroll for navigation links
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

// Typewriter effect
let text = "Technology Executive • Innovation Driver • Strategic Leader • Future CEO";
let i = 0;
let isTyping = true;

function typeWriter() {
    const element = document.getElementById("typing");

    if (isTyping) {
        if (i < text.length) {
            element.innerHTML += text.charAt(i);
            i++;
            setTimeout(typeWriter, 80);
        } else {
            isTyping = false;
            setTimeout(typeWriter, 2000); // Pause before erasing
        }
    } else {
        if (i > 0) {
            element.innerHTML = text.substring(0, i - 1);
            i--;
            setTimeout(typeWriter, 40);
        } else {
            isTyping = true;
            setTimeout(typeWriter, 500); // Pause before typing again
        }
    }
}

// Start typewriter effect when page loads
window.addEventListener('load', () => {
    setTimeout(typeWriter, 1000);
});

// Skill bar animations
function animateSkillBars() {
    const skillBars = document.querySelectorAll('.skill-fill');

    skillBars.forEach((bar, index) => {
        setTimeout(() => {
            const width = bar.style.width;
            bar.style.width = '0%';
            setTimeout(() => {
                bar.style.width = width;
            }, 200);
        }, index * 200);
    });
}

// Animate skill bars when skills section comes into view
const skillsSection = document.getElementById('skills');
const skillsObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            animateSkillBars();
            skillsObserver.unobserve(entry.target);
        }
    });
}, { threshold: 0.3 });

if (skillsSection) {
    skillsObserver.observe(skillsSection);
}

// Form submission handler
document.querySelector('.contact-form')?.addEventListener('submit', function(e) {
    e.preventDefault();

    // Simple form validation
    const name = this.querySelector('input[type="text"]').value;
    const email = this.querySelector('input[type="email"]').value;
    const message = this.querySelector('textarea').value;

    if (name && email && message) {
        // Here you would typically send the form data to a server
        alert('Thank you for your message! I will get back to you soon.');
        this.reset();
    } else {
        alert('Please fill in all fields.');
    }
});

// Add loading animation for images
document.querySelectorAll('img').forEach(img => {
    img.addEventListener('load', function() {
        this.style.opacity = '1';
    });
    img.style.opacity = '0';
    img.style.transition = 'opacity 0.5s ease';
});

// Parallax effect for hero background (subtle)
window.addEventListener('scroll', () => {
    const scrolled = window.pageYOffset;
    const heroBg = document.querySelector('.hero-bg');
    if (heroBg) {
        heroBg.style.transform = `translateY(${scrolled * 0.5}px)`;
    }
});

// Dynamic navigation highlight
window.addEventListener('scroll', () => {
    const sections = document.querySelectorAll('section');
    const navLinks = document.querySelectorAll('.nav-links a');

    let current = '';

    sections.forEach(section => {
        const sectionTop = section.offsetTop;
        const sectionHeight = section.clientHeight;

        if (pageYOffset >= sectionTop - sectionHeight / 3) {
            current = section.getAttribute('id');
        }
    });

    navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href').substring(1) === current) {
            link.classList.add('active');
        }
    });
});

// Add active class styles
const style = document.createElement('style');
style.textContent = `
    .nav-links a.active {
        color: #FFD700 !important;
    }
    .nav-links a.active::after {
        width: 100% !important;
    }
`;
document.head.appendChild(style);

</script>

</body>
</html>
