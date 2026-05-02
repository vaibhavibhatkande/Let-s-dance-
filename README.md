# Let-s-dance-
An attractive online dance class landing page built with HTML and internal CSS, featuring a full-screen ballerina background and an interactive Explore More button.
<!DOCTYPE html>
<html>

<head>
    <title>DANCE WEBSITE</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Slab&display=swap" rel="stylesheet">

    <style>
        * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
        }

        body {
            background-image: url('https://get.wallhere.com/photo/dancer-ballerina-ballet-street-1696427.jpg');
            background-size: cover;
            background-position: center;
            height: 100vh;
            font-family: 'Roboto Slab', serif;
        }

        /* Menu Bar */
        .menu-bar {
            background: rgba(0, 0, 0, 0.7);
            text-align: center;
            padding: 10px 0;
        }

        .menu-bar ul {
            display: inline-flex;
            list-style: none;
        }

        .menu-bar ul li {
            width: 120px;
            margin: 15px;
            padding: 15px;
            position: relative;
            transition: 0.3s;
        }

        .menu-bar ul li a {
            text-decoration: none;
            color: white;
            font-size: 14px;
            font-weight: bold;
        }

        .menu-bar ul li:hover {
            background: #2bab0d;
            border-radius: 5px;
        }

        /* Dropdown */
        .sub-menu-1 {
            display: none;
        }

        .menu-bar ul li:hover .sub-menu-1 {
            display: block;
            position: absolute;
            background: rgba(0, 100, 0, 0.9);
            margin-top: 15px;
            margin-left: -15px;
        }

        .menu-bar ul li:hover .sub-menu-1 ul {
            display: block;
            margin: 10px;
        }

        .menu-bar ul li:hover .sub-menu-1 ul li {
            width: 150px;
            padding: 10px;
            border-bottom: 1px dotted #fff;
            text-align: left;
        }

        .menu-bar ul li:hover .sub-menu-1 ul li:last-child {
            border-bottom: none;
        }

        .menu-bar ul li:hover .sub-menu-1 ul li a:hover {
            color: yellow;
        }

        /* Main Content */
        .main-content {
            text-align: center;
            color: white;
            margin-top: 120px;
        }

        .main-content h3 {
            font-size: 18px;
            letter-spacing: 3px;
        }

        .main-content h1 {
            font-size: 65px;
            margin: 20px 0;
            text-shadow: 2px 2px 10px black;
        }

        .main-content h4 {
            font-size: 18px;
            letter-spacing: 3px;
        }

        .main-content p {
            margin-top: 25px;
            font-size: 22px;
        }

        .login-btn {
            display: block;
            width: 50%;
            max-width: 250px;
            background: black;
            color: white;
            text-decoration: none;
            text-align: center;
            padding: 14px 0;
            border-radius: 30px;
            margin: 40px auto;
            font-size: 18px;
            transition: 0.5s;
        }

        .login-btn:hover {
            transform: scale(0.9);
            background: #2bab0d;
        }
    </style>
</head>

<body>

    <div class="menu-bar">
        <ul>
            <li><a href="#">TYPES</a>
                <div class="sub-menu-1">
                    <ul>
                        <li><a href="#">Ballet</a></li>
                        <li><a href="#">Hip Hop</a></li>
                        <li><a href="#">Contemporary</a></li>
                    </ul>
                </div>
            </li>

            <li><a href="#">GALLERY</a></li>
            <li><a href="#">ABOUT US</a></li>
            <li><a href="#">FEES</a></li>
            <li><a href="#">REGISTER</a></li>
            <li><a href="#">CONTACT</a></li>
        </ul>
    </div>

    <div class="main-content">
        <h3>IT IS NOT A JOKE</h3>
        <h1><u><i>LET'S DANCE</i></u></h1>
        <h4>IT IS POWER</h4>
        <p>Feel the rhythm, live the dance</p>

        <a href="#" class="login-btn">EXPLORE MORE</a>
    </div>

</body>

</html>
