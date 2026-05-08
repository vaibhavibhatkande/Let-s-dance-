<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elegant Neon Dance Academy</title>

    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap"
        rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #0f172a;
            color: white;
            overflow-x: hidden;
        }

        /* ================= NAVBAR ================= */

        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 18px 60px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(15, 23, 42, 0.88);
            backdrop-filter: blur(12px);
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
        }

        .logo {
            font-size: 30px;
            font-weight: 700;
            color: #ff4d8d;
            letter-spacing: 3px;
        }

        .navbar a {
            color: white;
            text-decoration: none;
            margin-left: 28px;
            transition: 0.3s;
            font-size: 15px;
        }

        .navbar a:hover {
            color: #ff4d8d;
        }

        /* ================= HOME ================= */

        .home {
            height: 100vh;
            background:
                linear-gradient(rgba(15, 23, 42, 0.65),
                    rgba(15, 23, 42, 0.82)),
                url('https://img.freepik.com/free-photo/spectrum-flashes-coloured-light_23-2151792482.jpg?semt=ais_hybrid&w=740&q=80');

            background-size: cover;
            background-position: center;

            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;

            text-align: center;
            padding: 20px;
        }

        .home h3 {
            color: #ffb3c7;
            letter-spacing: 4px;
            margin-bottom: 15px;
            font-weight: 400;
        }

        .home h1 {
            font-size: 90px;
            margin-bottom: 20px;
            line-height: 1.1;
        }

        .home h4 {
            color: #d1d5db;
            font-size: 18px;
            max-width: 650px;
            line-height: 1.8;
        }

        /* ================= BUTTON ================= */

        .btn,
        button,
        input[type=submit] {
            display: inline-block;
            margin-top: 30px;
            padding: 14px 38px;
            border: none;
            border-radius: 50px;
            background: linear-gradient(135deg, #ff4d8d, #7c3aed);
            color: white;
            text-decoration: none;
            font-weight: 600;
            cursor: pointer;
            transition: 0.4s;
            box-shadow: 0 10px 30px rgba(255, 77, 141, 0.3);
        }

        .btn:hover,
        button:hover,
        input[type=submit]:hover {
            transform: translateY(-5px);
        }

        /* ================= SECTION ================= */

        section {
            padding: 100px 8%;
        }

        .title {
            text-align: center;
            margin-bottom: 60px;
        }

        .title h2 {
            font-size: 45px;
            margin-bottom: 12px;
        }

        .title p {
            color: #cbd5e1;
        }

        /* ================= GALLERY ================= */

        .gallery-section {
            background: #111827;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 18px;
        }

        .gallery img {
            width: 260px;
            height: 190px;
            object-fit: cover;
            border-radius: 18px;
            transition: 0.5s;
            filter: grayscale(20%);
        }

        .gallery img:hover {
            transform: scale(1.08);
            filter: grayscale(0%);
            box-shadow: 0 15px 30px rgba(255, 77, 141, 0.35);
        }

        /* ================= ABOUT ================= */

        .about {
            background: #0f172a;
        }

        .wrapper {
            background: rgba(255, 255, 255, 0.05);
            margin: 30px auto;
            padding: 45px;
            width: 85%;
            border-radius: 25px;
            text-align: center;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .wrapper h2 {
            font-size: 40px;
            margin-bottom: 20px;
        }

        .wrapper p {
            color: #d1d5db;
            line-height: 1.9;
            font-size: 17px;
        }

        .wrapper img {
            width: 160px;
            margin: 25px 0;
        }

        /* ================= LOGIN ================= */

        .login-section {
            background: linear-gradient(135deg, #1e293b, #111827);
        }

        .container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 30px;
            overflow: hidden;
            width: 850px;
            max-width: 100%;
            min-height: 520px;
            position: relative;
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            margin: auto;
        }

        .form-container {
            position: absolute;
            top: 0;
            height: 100%;
            transition: all 0.6s ease-in-out;
        }

        .sign-in-container {
            left: 0;
            width: 50%;
            z-index: 2;
        }

        .sign-up-container {
            left: 0;
            width: 50%;
            opacity: 0;
            z-index: 1;
        }

        .container.right-panel-active .sign-in-container {
            transform: translateX(100%);
        }

        .container.right-panel-active .sign-up-container {
            transform: translateX(100%);
            opacity: 1;
            z-index: 5;
        }

        form {
            background: transparent;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 0 50px;
            height: 100%;
            text-align: center;
        }

        form h1 {
            margin-bottom: 25px;
            font-size: 35px;
        }

        input,
        textarea,
        select {
            width: 100%;
            padding: 14px 18px;
            margin: 10px 0;
            border: none;
            border-radius: 12px;
            background: rgba(255, 255, 255, 0.08);
            color: white;
            outline: none;
        }

        input::placeholder,
        textarea::placeholder {
            color: #cbd5e1;
        }

        textarea {
            resize: none;
            height: 150px;
        }

        .overlay-container {
            position: absolute;
            top: 0;
            left: 50%;
            width: 50%;
            height: 100%;
            overflow: hidden;
            transition: transform 0.6s ease-in-out;
            z-index: 100;
        }

        .container.right-panel-active .overlay-container {
            transform: translateX(-100%);
        }

        .overlay {
            background: linear-gradient(135deg, #ff4d8d, #7c3aed);
            color: white;
            position: relative;
            left: -100%;
            height: 100%;
            width: 200%;
            transition: transform 0.6s ease-in-out;
        }

        .container.right-panel-active .overlay {
            transform: translateX(50%);
        }

        .overlay-panel {
            position: absolute;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 0 40px;
            text-align: center;
            top: 0;
            height: 100%;
            width: 50%;
        }

        .overlay-left {
            transform: translateX(-20%);
        }

        .container.right-panel-active .overlay-left {
            transform: translateX(0);
        }

        .overlay-right {
            right: 0;
        }

        .container.right-panel-active .overlay-right {
            transform: translateX(20%);
        }

        .ghost {
            background: transparent;
            border: 2px solid white;
        }

        /* ================= CONTACT ================= */

        .contact-section {
            background: #0f172a;
        }

        .contact-box {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 25px;
            padding: 50px;
            width: 90%;
            margin: auto;
            backdrop-filter: blur(12px);
        }

        .contact-box p {
            text-align: center;
            margin-bottom: 40px;
            color: #d1d5db;
        }

        .row {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
        }

        .column {
            flex: 50%;
            padding: 20px;
        }

        .column img {
            width: 100%;
            border-radius: 25px;
        }

        /* ================= FOOTER ================= */

        .footer {
            background: #020617;
            color: #cbd5e1;
            text-align: center;
            padding: 25px;
            border-top: 1px solid rgba(255, 255, 255, 0.08);
        }

        /* ================= RESPONSIVE ================= */

        @media(max-width:768px) {

            .navbar {
                padding: 18px 20px;
            }

            .navbar a {
                margin-left: 12px;
                font-size: 13px;
            }

            .home h1 {
                font-size: 52px;
            }

            .title h2 {
                font-size: 34px;
            }

            .wrapper {
                width: 95%;
                padding: 30px;
            }

            .column {
                flex: 100%;
            }

            .contact-box {
                width: 95%;
                padding: 25px;
            }
        }
    </style>
</head>

<body>

    <!-- NAVBAR -->

    <div class="navbar">

        <div class="logo">DANCE</div>

        <div>
            <a href="#">Home</a>
            <a href="#gallery">Gallery</a>
            <a href="#about">About</a>
            <a href="#login">Login</a>
            <a href="#contact">Contact</a>
        </div>

    </div>

    <!-- HOME -->

    <section class="home">

        <h3>FEEL THE RHYTHM</h3>

        <h1>LET'S DANCE</h1>

        <h4>
            Discover the art of movement, passion,
            elegance and expression with our dance academy.
        </h4>

        <a href="#gallery" class="btn">Explore More</a>

    </section>

    <!-- GALLERY -->

    <section class="gallery-section" id="gallery">

        <div class="title">

            <h2>Dance Gallery</h2>

            <p>Moments filled with passion and energy</p>

        </div>

        <div class="gallery">

            <img src="https://images.unsplash.com/photo-1508804185872-d7badad00f7d">

            <img src="https://images.unsplash.com/photo-1515169067868-5387ec356754">

            <img src="https://images.unsplash.com/photo-1504609813442-a8924e83f76e">

            <img src="https://images.unsplash.com/photo-1516280440614-37939bbacd81">

            <img src="https://images.unsplash.com/photo-1499364615650-ec38552f4f34">

            <img src="https://images.unsplash.com/photo-1501386761578-eac5c94b800a">

            <img src="https://images.unsplash.com/photo-1508804185872-d7badad00f7d">

            <img src="https://images.unsplash.com/photo-1515169067868-5387ec356754">

            <img src="https://images.unsplash.com/photo-1508804185872-d7badad00f7d">

            <img src="https://images.unsplash.com/photo-1515169067868-5387ec356754">

            <img src="https://images.unsplash.com/photo-1504609813442-a8924e83f76e">

            <img src="https://images.unsplash.com/photo-1516280440614-37939bbacd81">

            <img src="https://images.unsplash.com/photo-1499364615650-ec38552f4f34">

            <img src="https://images.unsplash.com/photo-1501386761578-eac5c94b800a">

            <img src="https://images.unsplash.com/photo-1499364615650-ec38552f4f34">

            <img src="https://images.unsplash.com/photo-1501386761578-eac5c94b800a">


        </div>

    </section>

    <!-- ABOUT -->

    <section class="about" id="about">

        <div class="wrapper">

            <h2>Our Motive</h2>

            <p>
                “Everybody can dance, it's the drive and passion
                that makes you a dancer.”
            </p>

        </div>

        <div class="wrapper">

            <h2>About Us</h2>

            <img src="https://cdn-icons-png.flaticon.com/512/1995/1995574.png">

            <p>
                Dance is a universal art form that expresses emotion,
                creativity, and storytelling. Our academy helps you
                grow with confidence and passion.
            </p>

        </div>

    </section>

    <!-- LOGIN -->

    <section class="login-section" id="login">

        <div class="container" id="container">

            <!-- LOGIN FORM -->

            <div class="form-container sign-in-container">

                <form>

                    <h1>Login</h1>

                    <input type="text" placeholder="Username">

                    <input type="password" placeholder="Password">

                    <button type="submit">Login</button>

                </form>

            </div>

            <!-- REGISTER FORM -->

            <div class="form-container sign-up-container">

                <form>

                    <h1>Register</h1>

                    <input type="text" placeholder="Username">

                    <input type="email" placeholder="Email">

                    <input type="password" placeholder="Password">

                    <button type="submit">Register</button>

                </form>

            </div>

            <!-- OVERLAY -->

            <div class="overlay-container">

                <div class="overlay">

                    <div class="overlay-panel overlay-left">

                        <h1>Welcome Back!</h1>

                        <p>Please login with your personal info</p>

                        <button class="ghost" id="signIn">Sign In</button>

                    </div>

                    <div class="overlay-panel overlay-right">

                        <h1>Hello Dancer!</h1>

                        <p>Join us and start your journey</p>

                        <button class="ghost" id="signUp">Sign Up</button>

                    </div>

                </div>

            </div>

        </div>

    </section>

    <!-- CONTACT -->

    <section class="contact-section" id="contact">

        <div class="contact-box">

            <div class="title">

                <h2>Contact Us</h2>

                <p>We would love to hear from you</p>

            </div>

            <div class="row">

                <div class="column">

                    <img
                        src="https://images.unsplash.com/photo-1521791136064-7986c2920216?q=80&w=1200&auto=format&fit=crop">

                </div>

                <div class="column">

                    <form>

                        <input type="text" placeholder="First Name">

                        <input type="text" placeholder="Last Name">

                        <input type="email" placeholder="Email Address">

                        <textarea placeholder="Write your message..."></textarea>

                        <input type="submit" value="Send Message">

                    </form>

                </div>

            </div>

        </div>

    </section>

    <!-- FOOTER -->

    <div class="footer">

        © 2026 Elegant Dance Academy | Designed with Passion

    </div>

    <!-- JAVASCRIPT -->

    <script>

        const signUpButton = document.getElementById('signUp');
        const signInButton = document.getElementById('signIn');
        const container = document.getElementById('container');

        signUpButton.addEventListener('click', () => {
            container.classList.add("right-panel-active");
        });

        signInButton.addEventListener('click', () => {
            container.classList.remove("right-panel-active");
        });

    </script>

</body>

</html>
