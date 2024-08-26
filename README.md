<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern CV - Andi Irfan Maulana</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap&family=Roboto:wght@300;400&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            background: #f0f2f5;
            color: #333;
            scroll-behavior: smooth;
        }

        header {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #7f8c8d, #2980b9);
            color: white;
            text-align: center;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0% 100%);
            position: relative;
            overflow: hidden;
        }

        header h1 {
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 0.5em;
            letter-spacing: 2px;
        }

        header p {
            font-size: 1.3em;
            margin-top: 10px;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, #7f8c8d, #2980b9);
            z-index: -1;
            animation: gradientAnimation 8s ease infinite;
        }

        @keyframes gradientAnimation {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }

        nav {
            background-color: rgba(0, 0, 0, 0.5);
            position: fixed;
            top: 0;
            width: 100%;
            padding: 15px;
            text-align: center;
            z-index: 1000;
            backdrop-filter: blur(5px);
        }

        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-size: 1.1em;
            position: relative;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #f1c40f;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 50px 20px;
        }

        .section-title {
            font-size: 2.3em;
            color: #2980b9;
            text-align: center;
            margin-bottom: 30px;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 60px;
            height: 4px;
            background: #2980b9;
            display: block;
            margin: 15px auto 0;
        }

        .about,
        .experience,
        .skills,
        .contact {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 50px;
        }

        .about img {
            width: 300px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease;
        }

        .about img:hover {
            transform: scale(1.05);
        }

        .about-text {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .about-text h2 {
            font-size: 2em;
            color: #2980b9;
            margin-bottom: 10px;
        }

        .about-text p {
            font-size: 1.1em;
            color: #555;
            line-height: 1.6;
        }

        .skills {
            justify-content: space-around;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            padding: 30px;
        }

        .skill {
            text-align: center;
            flex: 1;
            margin: 10px;
            background: #f5f7fa;
            padding: 20px;
            border-radius: 15px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .skill:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 30px rgba(0, 0, 0, 0.15);
        }

        .experience {
            flex-direction: column;
            gap: 20px;
        }

        .experience-item {
            background: white;
            border: 2px solid #2980b9;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .experience-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .experience-item h3 {
            font-size: 1.8em;
            color: #2980b9;
            margin-bottom: 10px;
        }

        .experience-item p {
            font-size: 1.1em;
            color: #555;
        }

        .contact {
            justify-content: space-around;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            padding: 30px;
            text-align: center;
        }

        .contact h2 {
            font-size: 2em;
            color: #2980b9;
            margin-bottom: 20px;
        }

        .social a {
            display: inline-block;
            margin: 0 15px;
            transition: transform 0.3s, filter 0.3s;
        }

        .social img {
            width: 50px;
        }

        .social a:hover {
            transform: scale(1.2);
            filter: brightness(1.2);
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
        }

        footer p {
            margin: 0;
        }

        @media (max-width: 768px) {
            header {
                height: 70vh;
                clip-path: none;
            }

            header h1 {
                font-size: 2.5em;
            }

            header p {
                font-size: 1.2em;
            }

            .about {
                flex-direction: column;
                align-items: center;
            }

            .about img {
                width: 100%;
                max-width: 300px;
            }

            .about-text {
                text-align: center;
                padding: 15px;
            }

            .skills,
            .contact {
                flex-direction: column;
                align-items: center;
            }

            .skill {
                margin: 20px 0;
            }

            .social img {
                width: 40px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Andi Irfan Maulana</h1>
        <p>Web Developer & Professional Event Organizer</p>
        <!-- Background Music -->
        <audio autoplay loop muted>
            <source src="musik.mp3" type="audio/mp3">
            Your browser does not support the audio element.
        </audio>
    </header>

    <nav>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
    </nav>

    <div class="container">
        <section id="about" class="about">
            <img src="edit2.jpg" alt="Profile Picture">
            <div class="about-text">
                <h2>About Me</h2>
                <p>I am a passionate web developer with over 5 years of experience in creating dynamic and responsive websites...</p>
            </div>
        </section>

        <section id="skills" class="skills">
            <div class="skill">
                <h3>Web Development</h3>
                <p>Expertise in HTML, CSS, JavaScript.</p>
            </div>
            <div class="skill">
                <h3>Design</h3>
                <p>CorelDraw, Adobe Photoshop, Illustrator.</p>
            </div>
            <div class="skill">
                <h3>Microsoft</h3>
                <p>Excel, Word, PowerPoint.</p>
            </div>
        </section>

        <section id="experience" class="experience">
            <h2 class="section-title">Experience</h2>
            <div class="experience-item">
                <h3>Team Leader PT. Yasika Production</h3>
                <p>Mengelola dan memimpin tim, memberikan bimbingan, menyelesaikan masalah di lapangan, mengevaluasi kerja tim.</p>
            </div>
            <div class="experience-item">
                <h3>Project Officer PT. Color Production</h3>
                <p>Koordinasi antar pemangku kepentingan, membuat perencanaan dan pengawasan, mengembangkan strategi mitigasi dan manajemen risiko.</p>
            </div>
            <div class="experience-item">
                <h3>Area Sales Manager PT. MultiBintang Tbk.</h3>
                <p>Koordinasi antar pemangku kepentingan, membuat perencanaan dan pengawasan, mengembangkan strategi mitigasi dan manajemen risiko.</p>
            </div>
            <div class="experience-item">
                <h3>Head Of Team PT. Ghaisan Utama Indomedia</h3>
                <p>Koordinasi antar pemangku kepentingan, membuat perencanaan dan pengawasan, mengembangkan strategi mitigasi dan manajemen risiko.</p>
            </div>
            <div class="experience-item">
                <h3>Web Development</h3>
                <p>Memimpin proyek desain dari konsep hingga penyelesaian, dengan fokus pada penciptaan antarmuka yang intuitif dan menarik secara visual...</p>
            </div>
        </section>

        <section id="contact" class="contact">
            <h2 class="section-title">Hubungi Saya</h2>
            <div class="social">
                <a href="https://wa.me/+6285345674445" target="_blank"><img src="w.png" alt="WhatsApp"></a>
                <a href="https://www.instagram.com/andiirfanmaulana" target="_blank"><img src="i.png" alt="Instagram"></a>
                <a href="mailto:andiirfan1020@gmail.com" target="_blank"><img src="g.png" alt="Email"></a>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 Andi Irfan Maulana. All rights reserved.</p>
    </footer>
</body>
</html>
