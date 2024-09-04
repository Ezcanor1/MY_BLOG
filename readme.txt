/your-blog
    /assets
        /css
            - styles.css
        /js
            - script.js
        /images
    index.html









css


/* General Styles */
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
    transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
}

a {
    text-decoration: none;
    color: inherit;
    transition: color 0.3s ease-in-out;
}

header {
    background-color: #000;
    padding: 20px 40px;
    color: #fff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: background-color 0.3s ease-in-out;
}

.logo {
    font-size: 1.5em;
    font-weight: bold;
    transition: transform 0.3s ease-in-out;
}

.logo:hover {
    transform: scale(1.1);
}

.nav-links {
    list-style: none;
    display: flex;
}

.nav-links li {
    margin-left: 20px;
    opacity: 0;
    animation: fadeIn 0.5s forwards;
}

.nav-links li:nth-child(1) { animation-delay: 0.2s; }
.nav-links li:nth-child(2) { animation-delay: 0.4s; }
.nav-links li:nth-child(3) { animation-delay: 0.6s; }
.nav-links li:nth-child(4) { animation-delay: 0.8s; }

.nav-links a {
    color: #fff;
    padding: 8px 12px;
    transition: background 0.3s ease-in-out, color 0.3s ease-in-out;
}

.nav-links a:hover {
    background-color: #555;
    border-radius: 4px;
    color: #f1f1f1;
}

.burger {
    display: none;
    cursor: pointer;
}

.burger div {
    width: 25px;
    height: 3px;
    background-color: #fff;
    margin: 5px;
    transition: all 0.3s ease-in-out;
}

.burger.toggle .line1 {
    transform: rotate(-45deg) translate(-5px, 5px);
}

.burger.toggle .line2 {
    opacity: 0;
}

.burger.toggle .line3 {
    transform: rotate(45deg) translate(-5px, -5px);
}

.hero {
    background: url('assets/images/hero.jpg') no-repeat center center/cover;
    height: 60vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    text-align: center;
    padding: 0 20px;
    animation: fadeInHero 1s ease-in-out;
}

.hero h1 {
    font-size: 3em;
    margin-bottom: 20px;
    animation: fadeInDown 1s ease-in-out;
}

.cta-button {
    background-color: #007bff;
    padding: 10px 20px;
    color: #fff;
    border-radius: 4px;
    transition: background 0.3s ease-in-out, transform 0.3s ease-in-out;
    animation: fadeInUp 1s ease-in-out;
}

.cta-button:hover {
    background-color: #0056b3;
    transform: scale(1.05);
}

.blog-section {
    padding: 60px 20px;
    text-align: center;
    transition: padding 0.3s ease-in-out;
}

.posts-container {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    transition: all 0.3s ease-in-out;
}

.post {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    overflow: hidden;
    margin: 20px;
    max-width: 300px;
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.post:hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.post img {
    width: 100%;
    height: auto;
    transition: transform 0.3s ease-in-out;
}

.post img:hover {
    transform: scale(1.05);
}

.post-content {
    padding: 20px;
    transition: padding 0.3s ease-in-out;
}

.read-more {
    display: inline-block;
    margin-top: 10px;
    color: #007bff;
    transition: color 0.3s ease-in-out, transform 0.3s ease-in-out;
}

.read-more:hover {
    color: #0056b3;
    transform: translateX(5px);
}

footer {
    background-color: #000;
    color: #fff;
    text-align: center;
    padding: 20px 0;
    transition: background-color 0.3s ease-in-out;
}

.social-links {
    list-style: none;
    padding: 0;
    margin: 10px 0 0;
    display: flex;
    justify-content: center;
}

.social-links li {
    margin: 0 10px;
    opacity: 0;
    animation: fadeIn 0.5s forwards;
}

.social-links li:nth-child(1) { animation-delay: 0.2s; }
.social-links li:nth-child(2) { animation-delay: 0.4s; }
.social-links li:nth-child(3) { animation-delay: 0.6s; }

/* Keyframes */
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

@keyframes fadeInHero {
    from { opacity: 0; transform: scale(0.95); }
    to { opacity: 1; transform: scale(1); }
}

@keyframes fadeInDown {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

/* Responsive Styles */
@media (max-width: 768px) {
    .nav-links {
        display: none;
        flex-direction: column;
        background-color: #000;
        position: absolute;
        top: 60px;
        right: 0;
        width: 200px;
        padding: 20px;
        transition: right 0.3s ease-in-out, opacity 0.3s ease-in-out;
    }

    .burger {
        display: block;
    }

    .nav-active {
        display: flex;
    }

    .hero {
        height: 50vh;
    }
}











html


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Blog Name</title>
    <link rel="stylesheet" href="assets/css/styles.css">
    <link rel="icon" href="assets/images/favicon.ico">
</head>
<body>
    <header>
        <nav>
            <div class="logo">Your Blog</div>
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
            <div class="burger">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
        </nav>
    </header>
    
    <main>
        <section class="hero">
            <div class="hero-content">
                <h1>Welcome to Your Blog</h1>
                <p>Sharing knowledge, insights, and experiences.</p>
                <a href="#blog-posts" class="cta-button">Explore Posts</a>
            </div>
        </section>
        
        <section id="blog-posts" class="blog-section">
            <h2>Latest Posts</h2>
            <div class="posts-container">
                <!-- Blog posts will go here -->
                <article class="post">
                    <img src="assets/images/post1.jpg" alt="Post Image">
                    <div class="post-content">
                        <h3>Post Title 1</h3>
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                        <a href="#" class="read-more">Read More</a>
                    </div>
                </article>
                <!-- Repeat for more posts -->
            </div>
        </section>
    </main>
    
    <footer>
        <div class="footer-content">
            <p>&copy; 2024 Your Blog. All rights reserved.</p>
            <ul class="social-links">
                <li><a href="#">Twitter</a></li>
                <li><a href="#">Facebook</a></li>
                <li><a href="#">LinkedIn</a></li>
            </ul>
        </div>
    </footer>

    <script src="assets/js/script.js"></script>
</body>
</html>












java script


document.querySelector('.burger').addEventListener('click', () => {
    document.querySelector('.nav-links').classList.toggle('nav-active');
    document.querySelector('.burger').classList.toggle('toggle');
});
