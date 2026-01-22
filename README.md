<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="I am Omar Yasser Elattar from Egypt, studying in Millennium Language School">

    <title>Omar Elattar</title>

    <style>
        * {
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }

        body {
            margin: 0;
            background-color: #f4f4f4;
            color: #333;
        }

        .container {
            width: 90%;
            max-width: 900px;
            margin: auto;
            padding: 20px;
        }

        header {
            text-align: center;
        }

        header img {
            border-radius: 50%;
            margin: 15px 0;
        }

        .name { color: brown; }
        .school { color: red; }
        .work-video { color: orange; }
        .work-design { color: blue; }
        .work-podcast { color: chartreuse; }

        hr {
            width: 80%;
            margin: 30px auto;
        }

        section h3 {
            border-left: 5px solid #333;
            padding-left: 10px;
        }

        .social a {
            display: inline-block;
            margin: 5px 10px 5px 0;
            text-decoration: none;
            color: #0066cc;
        }

        .social a:hover {
            text-decoration: underline;
        }

        ul {
            margin-left: 20px;
        }

        footer {
            text-align: center;
            font-size: 14px;
            color: #666;
        }
    </style>
</head>

<body>

<header class="container">
    <h1>Omar Elattar</h1>

    <img src="./photo.jpg" width="150" height="150" alt="Omar photo">

    <p>
        <b><span class="name">Omar Yasser Elattar</span></b><br>
        <u>Studies</u> in <b class="school">M.L.S</b><br>
        <u>Works</u> in <span class="work-video">Video Montage</span> and <b class="work-design">Photoshop</b><br>
        <u>Writes</u> <span class="work-podcast">Podcasts</span>
    </p>
</header>

<hr>

<main class="container">

<section id="contact-us">
    <h3>Contact Me</h3>

    <!-- FORM CODE (UNCHANGED) -->
    <form action = "https://formsubmit.co/omarelattar308@gmail.com" method = post>
        <div id = name></div>
        <input type = text placeholder = Name required>
        <br><br>
        <div id = password></div>
        <input type = password placeholder = Password required>
        <br><br>
        <div id = message></div>
        <textarea name ="Discribe your request" Cols ="30" rows = "10" placeholder="Message" ></textarea>
        <br>  

        <p><h4>Gendre</h4></p>

        <input type = radio name = gendre>
        <label>Male</label>
        <br><br>
        <input type = radio name = gendre >
        <label>Female</label>
        <br><br>

        <p><h4>Country</h4></p>

        <select>
            <option value = "1" selected >Egypt</option>
            <option value = "1">Qutar</option>
            <option value = "1">Suadi Arabia</option>
            <option value = "1">Morocco</option>
        </select>

        <p><h4>I can help you with</h4></p>

        <input type = checkbox name = work >
        <label>Podcast</label>
        <br><br>
        <input type =checkbox name = work >
        <label>Photo Graphic Designing </label>
        <br><br>
        <input type =checkbox name = work >
        <label>Video montage</label>
        <br><br>
        <input type =checkbox name = work >
        <label>Sponser</label>
        <br><br>
        <input type = submit >
    </form>

    <hr>

    <p>
        <b>Phone number</b>: +201027795920 <br>
        <b>Telegram</b>:
    </p>

    <div class="social">
        <a href="https://www.facebook.com/profile.php?id=100051007188187">Facebook</a>
        <a href="https://www.instagram.com/invites/contact/?i=19g9l84b0qlru&utm_content=jk06eyb">Instagram</a>
        <a href="https://www.tiktok.com/@o_el3attar">TikTok</a>
        <a href="mailto:omarelattar308@gmail.com">Gmail</a>
    </div>
</section>

<hr>

<section id="about-me">
    <h3>About Me</h3>

    <h4>My Skills</h4>

    <ul>
        <li>Programming
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>Python</li>
            </ul>
        </li>
        <li>Montage</li>
        <li>Designing</li>
        <li>Writing</li>
        <li>Studying Psychology</li>
    </ul>
</section>

</main>

<footer class="container">
    <p>All rights are preserved &copy;</p>
</footer>

</body>
</html>
