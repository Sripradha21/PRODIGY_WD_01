<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <style>
        /* Basic Reset */
        body, html {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        /* Navigation Bar */
        nav {
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            background-color: #333;
            padding: 10px 0;
            z-index: 1000;
            transition: background-color 0.3s;
        }

        nav.scrolled {
            background-color: #222;
        }

        .menu {
            list-style: none;
            display: flex;
            justify-content: center;
            margin: 0;
            padding: 0;
        }

        .menu li {
            margin: 0 15px;
        }

        .menu li a {
            text-decoration: none;
            color: white;
            font-size: 18px;
            transition: color 0.3s;
        }

        .menu li a:hover {
            color: #FFD700; /* Gold color when hovered */
        }

        /* Section Styling */
        section {
            padding: 100px 20px;
            min-height: 100vh;
            text-align: center;
        }

        #home { background-color: #f4f4f4; }
        #about { background-color: #ddd; }
        #services { background-color: #bbb; }
        #contact { background-color: #999; }

        /* Ensuring spacing at the top for visibility */
        body {
            padding-top: 60px;
        }
    </style>
</head>
<body>
    <nav id="navbar">
        <ul class="menu">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home">
        <h1>Welcome to Home</h1>
        <p>This is the home section. Scroll down to explore more sections.</p>
    </section>
    <section id="about">
        <h1>About Us</h1>
        <p>Learn more about us in this section.</p>
    </section>
    <section id="services">
        <h1>Our Services</h1>
        <p>Discover our services here.</p>
    </section>
    <section id="contact">
        <h1>Contact Us</h1>
        <p>Get in touch with us through this section.</p>
    </section>

    <script>
        // Change the navbar background when scrolling
        window.onscroll = function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        };
    </script>
</body>
</html>
