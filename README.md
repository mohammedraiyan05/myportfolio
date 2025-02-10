<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            font-family: Arial, sans-serif;
            background-color: #2c2f33;
            color: white;
        }

        .sidebar {
            width: 250px;
            background-color: #1c1e22;
            padding: 20px;
            height: 100vh;
            position: fixed;
            left: 0;
            top: 0;
            transition: 0.3s;
        }
        .sidebar h2 {
            color: #00ffcc;
            text-align: center;
        }
        .sidebar ul {
            list-style: none;
            padding: 0;
        }
        .sidebar ul li {
            margin: 15px 0;
            position: relative;
        }
        .sidebar ul li a {
            text-decoration: none;
            color: white;
            display: block;
            padding: 10px;
            border-radius: 5px;
            background-color: #444;
            transition: 0.3s;
        }
        .sidebar ul li a:hover {
            background-color: #00ffcc;
            color: #000;
        }
        .dropdown {
            display: none;
            flex-direction: column;
            background-color: #333;
            position: absolute;
            left: 100%;
            top: 0;
            width: 180px;
            padding: 10px;
            border-radius: 5px;
        }
        .sidebar ul li:hover .dropdown {
            display: flex;
        }
        .main-content {
            margin-left: 270px;
            padding: 40px;
            flex: 1;
            background-color: #282b30;
            transition: background-color 0.3s;
        }

        .home-content {
            text-align: center;
            padding: 50px;
        }

        .home-content h1 {
            font-size: 36px;
            color: #00ffcc;
            text-shadow: 2px 2px 5px rgba(0, 255, 204, 0.5);
        }

        .home-content p {
            font-size: 18px;
            max-width: 600px;
            margin: auto;
            line-height: 1.6;
        }

        .skills {
            text-align: center;
            padding: 50px;
        }

        .skills h2 {
            font-size: 30px;
            color: #00ffcc;
            text-shadow: 1px 1px 3px rgba(0, 255, 204, 0.5);
        }

        .skills p {
            font-size: 18px;
            line-height: 1.6;
            max-width: 800px;
            margin: auto;
            padding: 0 20px; /* Added padding for better readability */
        }

        .projects {
            text-align: center;
            padding: 50px;
        }

        .projects h2 {
            font-size: 30px;
            color: #00ffcc;
            text-shadow: 1px 1px 3px rgba(0, 255, 204, 0.5);
        }

        .project-box {
            background-color: #444;
            padding: 20px;
            border-radius: 10px;
            margin: 20px auto;
            width: 80%;
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative; /* Added for positioning effects */
            overflow: hidden; /* Hide overflow for aesthetic */
        }

        .project-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 20px rgba(0, 255, 204, 0.5);
        }

        .project-box h3 {
            color: #00ffcc;
            margin: 10px 0;
            font-size: 24px; /* Increased font size */
        }

        .project-box p {
            line-height: 1.6;
            font-size: 16px; /* Slightly smaller font size */
        }

        .contact {
            text-align: center;
            padding: 50px;
        }

        .contact h2 {
            font-size: 30px;
            color: #00ffcc;
            text-shadow: 1px 1px 3px rgba(0, 255, 204, 0.5);
        }

        .contact p {
            font-size: 18px;
            line-height: 1.6;
            max-width: 600px;
            margin: auto;
        }

        .contact a {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            color: white;
            background-color: #00ffcc;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s, transform 0.2s; /* Added transform transition */
            font-weight: bold; /* Bold text for visibility */
        }

        .contact a:hover {
            background-color: #00ccaa;
            transform: scale(1.05); /* Slightly enlarge the button on hover */
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .sidebar {
                width: 220px;
            }

            .main-content {
                margin-left: 240px;
                padding: 20px;
            }

            .home-content h1 {
                font-size: 28px;
            }

            .skills h2,
            .projects h2,
            .contact h2 {
                font-size: 24px;
            }

            .project-box {
                width: 90%;
            }
        }

        @media (max-width: 480px) {
            .sidebar {
                display: none;
            }

            .main-content {
                margin-left: 0;
                padding: 10px;
            }

            .home-content h1 {
                font-size: 24px; /* Reducing heading size */
            }
        }
    </style>
</head>

<body>
    <div class="sidebar">
        <h2>My Portfolio</h2>
        <ul>
            <li><a href="main.html">🏠 Home</a></li>
            <li><a href="about.html">👤 About Me</a></li>
            <li><a href="services.html">📋 Services</a></li>
            <li>
                <a href="gallery.html">🖼 Gallery &#8594</a>
                <div class="dropdown">
                    <a href="certificates.html">🏅 Certificates</a>
                    <a href="achievements.html">🏆 Achievements</a>
                </div>
            </li>
            <li><a href="contact.html">💬 Contact Me</a></li>
        </ul>
    </div>
    <div class="main-content">
        <div class="home-content">
            <h1>Welcome to My Portfolio</h1>
            <p>Hello! I'm a passionate web developer dedicated to crafting visually appealing and functional websites. I specialize in front-end and back-end development, ensuring seamless digital experiences.</p>
        </div>

        <div class="skills">
            <h2>Skills</h2>
            <p>My skill set includes proficiency in HTML, CSS, JavaScript, Python, and MySQL. I am also familiar with database management and version control systems like Git.</p>
        </div>

        <div class="projects">
            <h2>Recent Projects</h2>
            <div class="project-box">
                <h3>Personal Portfolio Website</h3>
                <p>A responsive portfolio website to showcase my skills and projects, built using HTML, CSS, and JavaScript.</p>
            </div>
            <div class="project-box">
                <h3>College/School Management System</h3>
                <p>A comprehensive management system for educational institutions, built with PHP and MySQL, allowing for student enrollment, attendance tracking, and marks allocation.</p>
            </div>
            <div class="project-box">
                <h3>Blog Platform</h3>
                <p>A blogging platform enabling users to create, edit, and comment on posts, built with Express and MongoDB.</p>
            </div>
        </div>

        <div class="contact">
            <h2>Contact Me</h2>
            <p>If you have any questions or would like to discuss a project, feel free to reach out!</p>
            <a href="contact.html">📩 Get in Touch</a>
        </div>
    </div>
</body>

</html>
