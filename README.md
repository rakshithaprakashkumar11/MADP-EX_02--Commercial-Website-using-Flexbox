# Ex02 Commercial Website
## Date:

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM

## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wanderlust Adventures</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
</head>
<body>
  <header>
    <div class="logo">Wanderlust</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#destinations">Destinations</a>
      <a href="#about">About</a>
      <a href="#contact" class="btn">Contact</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <div class="hero-text">
      <h1>Explore The World</h1>
      <p>Unforgettable journeys, breathtaking destinations, and memories for a lifetime.</p>
      <a href="#destinations" class="btn">Start Your Adventure</a>
    </div>
    <div class="hero-image">
      <img src="download.jpeg" alt="Scenic travel view">
    </div>
  </section>

  <section class="destinations" id="destinations">
    <h2>Top Destinations</h2>
    <div class="destination-grid">
      <div class="destination-card">
        <img src="paris.jpg" alt="Paris">
        <h3>Paris, France</h3>
        <p>The city of lights, romance, and timeless charm.</p>
      </div>
      <div class="destination-card">
        <img src="bali.jpeg" alt="Bali">
        <h3>Bali, Indonesia</h3>
        <p>Pristine beaches, lush greenery, and serene temples.</p>
      </div>
      <div class="destination-card">
        <img src="newyork.jpeg" alt="New York City">
        <h3>New York City, USA</h3>
        <p>The bustling metropolis full of culture, food, and life.</p>
      </div>
    </div>
  </section>

  <section class="about" id="about">
    <div class="about-container">
      <div class="about-image">
        <img src="adventure-travel.avif" alt="Adventure travel">
      </div>
      <div class="about-text">
        <h2>About Wanderlust Adventures</h2>
        <p>
          At <strong>Wanderlust Adventures</strong>, we believe travel is more than just visiting places — it's about creating stories. 
          From luxurious getaways to rugged backpacking trips, we craft experiences for every kind of traveler.
        </p>
        <p>
          Our team of travel experts works around the clock to ensure your journey is smooth, safe, and full of joy.
        </p>
        <a href="#contact" class="btn">Plan Your Trip</a>
      </div>
    </div>
  </section>

  <section class="contact" id="contact">
    <h2>Contact Us</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>© 2025 Wanderlust Adventures. All rights reserved.</p>
  </footer>
</body>
</html>
```
## style.css
```
:root {
  --primary: #1e88e5;
  --secondary: #e3f2fd;
  --accent: #29b6f6;
  --text-dark: #1a237e;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  color: var(--text-dark);
  background-color: var(--secondary);
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background-color: white;
  box-shadow: 0 2px 10px rgba(0,0,0,0.05);
}

.logo {
  font-family: 'Pacifico', cursive;
  font-size: 28px;
  color: var(--primary);
}

nav a {
  margin: 0 15px;
  text-decoration: none;
  color: var(--text-dark);
  font-weight: 500;
}

nav a.btn {
  background: var(--primary);
  color: white;
  padding: 8px 15px;
  border-radius: 6px;
}

.hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  padding: 50px;
  align-items: center;
  gap: 20px;
}

.hero-text h1 {
  font-size: 48px;
  color: var(--primary);
}

.hero-text p {
  margin: 20px 0;
}

.hero-text .btn {
  background: var(--accent);
  color: white;
  padding: 10px 18px;
  border-radius: 6px;
  text-decoration: none;
}

.hero-image img {
  width: 100%;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
}

.destinations {
  text-align: center;
  padding: 50px 20px;
}

.destinations h2 {
  margin-bottom: 30px;
  font-size: 32px;
}

.destination-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
  gap: 20px;
}

.destination-card {
  background: white;
  border-radius: 12px;
  padding: 15px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.05);
}

.destination-card img {
  width: 100%;
  border-radius: 10px;
  margin-bottom: 15px;
}

.about {
  padding: 60px 20px;
}

.about-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 40px;
  max-width: 1100px;
  margin: auto;
}

.about-image img {
  width: 100%;
  border-radius: 12px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
}

.about-text h2 {
  font-size: 36px;
  margin-bottom: 20px;
  color: var(--primary);
}

.about-text p {
  margin-bottom: 15px;
  line-height: 1.6;
}

.about-text .btn {
  background: var(--accent);
  color: white;
  padding: 10px 20px;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 600;
  display: inline-block;
  transition: background 0.3s ease;
}

.about-text .btn:hover {
  background: #0288d1;
}

.contact {
  padding: 50px 20px;
  text-align: center;
}

.contact form {
  max-width: 400px;
  margin: auto;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.contact input,
.contact textarea {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 6px;
}

.contact button {
  background: var(--primary);
  color: white;
  padding: 10px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}

footer {
  text-align: center;
  padding: 20px;
  background: white;
  box-shadow: 0 -2px 10px rgba(0,0,0,0.05);
  margin-top: 30px;
}

@media (max-width: 768px) {
  .hero {
    grid-template-columns: 1fr;
  }
}
```



## OUTPUT
<img width="1899" height="913" alt="image" src="https://github.com/user-attachments/assets/ceb2ece1-c7d8-4c48-a88c-65338cb40abe" />
<img width="1892" height="889" alt="image" src="https://github.com/user-attachments/assets/0deb7dea-b793-44ea-ba2d-f50c907e3d46" />
<img width="1875" height="880" alt="image" src="https://github.com/user-attachments/assets/6eb66205-d123-4333-8abf-99b08bbf71de" />




## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
