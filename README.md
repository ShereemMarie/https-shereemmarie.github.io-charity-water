<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Your Brand Landing Page</title>
  <link
    href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap"
    rel="stylesheet"
  />
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- NAVIGATION -->
  <nav class="nav container">
    <a href="#" class="logo">YourLogo</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#features">Features</a></li>
      <li><a href="#cta">Get Started</a></li>
    </ul>
  </nav>

  <!-- HERO SECTION -->
  <header class="hero container">
    <div class="hero-text">
      <h1>Clean Water. Lasting Impact.</h1>
      <p>
        Bring safe, sustainable water to communities worldwide. Join us in
        making a difference—drop by drop.
      </p>
      <a href="#cta" class="btn primary-btn">Donate Now</a>
    </div>
    <div class="hero-image">
      <img
        src="https://via.placeholder.com/600x400"
        alt="Community gathering water"
      />
    </div>
  </header>

  <!-- ABOUT SECTION -->
  <section id="about" class="about container">
    <h2>Our Mission</h2>
    <p>
      charity: water is a nonprofit bringing clean, safe drinking water to
      people in developing countries. Since 2006, we’ve funded over 67,000
      water projects for more than 15 million people.
    </p>
  </section>

  <!-- FEATURES / IMPACT STATS -->
  <section id="features" class="features container">
    <div class="feature">
      <h3>15M+</h3>
      <p>People Served</p>
    </div>
    <div class="feature">
      <h3>67K+</h3>
      <p>Projects Funded</p>
    </div>
    <div class="feature">
      <h3>97¢</h3>
      <p>Every Dollar to Water</p>
    </div>
  </section>

  <!-- CTA SECTION -->
  <section id="cta" class="cta container">
    <h2>Ready to Make a Difference?</h2>
    <p>Your gift brings hope, health, and opportunity to those in need.</p>
    <a href="#" class="btn accent-btn">Give Today</a>
  </section>

  <!-- FOOTER -->
  <footer class="footer container">
    <div class="footer-col">
      <h4>charity: water</h4>
      <p>1234 Hope Ave, New York, NY 10001</p>
    </div>
    <div class="footer-col">
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#features">Impact</a></li>
        <li><a href="#cta">Donate</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Follow Us</h4>
      <ul class="social">
        <li><a href="#">Twitter</a></li>
        <li><a href="#">Facebook</a></li>
        <li><a href="#">Instagram</a></li>
      </ul>
    </div>
  </footer>

</body>
</html>
/* 1. RESET & VARIABLES */
:root {
  --clr-green-primary:   #8bc34a;
  --clr-green-light:     #dcedc8;
  --clr-blue-light:      #b3e5fc;
  --clr-white:           #ffffff;
  --clr-text:            #333333;

  --fw-normal: 400;
  --fw-bold:   600;
}
* {
  margin: 0; padding: 0; box-sizing: border-box;
}
body {
  font-family: 'Montserrat', sans-serif;
  color: var(--clr-text);
  background: var(--clr-white);
  line-height: 1.6;
}

/* 2. UTILITY */
.container {
  width: min(90%, 1000px);
  margin: 0 auto;
}
h1, h2, h3, h4 {
  font-weight: var(--fw-bold);
}
p {
  margin-bottom: 1rem;
}
.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 4px;
  text-decoration: none;
  font-weight: var(--fw-bold);
  transition: opacity 0.2s;
}
.btn:hover {
  opacity: 0.9;
}

/* 3. NAVIGATION */
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
}
.logo {
  font-size: 1.25rem;
  color: var(--clr-green-primary);
  text-decoration: none;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}
.nav-links a {
  text-decoration: none;
  color: var(--clr-text);
}

/* 4. HERO */
.hero {
  display: flex;
  flex-direction: column-reverse;
  gap: 2rem;
  padding: 2rem 0;
  align-items: center;
}
.hero-text h1 {
  font-size: 2rem;
  color: var(--clr-green-primary);
}
.hero-text p {
  font-size: 1rem;
}
.primary-btn {
  background: var(--clr-green-primary);
  color: var(--clr-white);
}
.hero-image img {
  width: 100%;
  border-radius: 8px;
}
@media (min-width: 768px) {
  .hero {
    flex-direction: row;
    text-align: left;
  }
  .hero-text, .hero-image {
    flex: 1;
  }
}

/* 5. ABOUT */
.about {
  text-align: center;
  padding: 3rem 0;
}
.about h2 {
  font-size: 1.75rem;
  color: var(--clr-blue-light);
  margin-bottom: 1rem;
}

/* 6. FEATURES */
.features {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  text-align: center;
  padding: 3rem 0;
}
@media (min-width: 600px) {
  .features {
    grid-template-columns: repeat(3, 1fr);
  }
}
.feature h3 {
  font-size: 2rem;
  color: var(--clr-green-primary);
}
.feature p {
  font-size: 0.9rem;
  color: var(--clr-text);
}

/* 7. CTA */
.cta {
  background: var(--clr-blue-light);
  text-align: center;
  padding: 3rem 0;
}
.cta h2 {
  font-size: 1.75rem;
  margin-bottom: 0.5rem;
}
.accent-btn {
  background: var(--clr-green-primary);
  color: var(--clr-white);
}

/* 8. FOOTER */
.footer {
  display: grid;
  gap: 2rem;
  padding: 3rem 0;
  background: var(--clr-green-light);
}
.footer-col h4 {
  margin-bottom: 0.5rem;
  color: var(--clr-text);
}
.footer-col p, .footer-col a {
  font-size: 0.9rem;
  color: var(--clr-text);
  text-decoration: none;
}
.footer .social {
  list-style: none;
  display: flex;
  gap: 1rem;
}
@media (min-width: 600px) {
  .footer {
    grid-template-columns: repeat(3, 1fr);
  }
}
/* 1. RESET & VARIABLES */
:root {
  --clr-green-primary:   #8bc34a;
  --clr-green-light:     #dcedc8;
  --clr-blue-light:      #b3e5fc;
  --clr-white:           #ffffff;
  --clr-text:            #333333;

  --fw-normal: 400;
  --fw-bold:   600;
}
* {
  margin: 0; padding: 0; box-sizing: border-box;
}
body {
  font-family: 'Montserrat', sans-serif;
  color: var(--clr-text);
  background: var(--clr-white);
  line-height: 1.6;
}

/* 2. UTILITY */
.container {
  width: min(90%, 1000px);
  margin: 0 auto;
}
h1, h2, h3, h4 {
  font-weight: var(--fw-bold);
}
p {
  margin-bottom: 1rem;
}
.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 4px;
  text-decoration: none;
  font-weight: var(--fw-bold);
  transition: opacity 0.2s;
}
.btn:hover {
  opacity: 0.9;
}

/* 3. NAVIGATION */
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
}
.logo {
  font-size: 1.25rem;
  color: var(--clr-green-primary);
  text-decoration: none;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}
.nav-links a {
  text-decoration: none;
  color: var(--clr-text);
}

/* 4. HERO */
.hero {
  display: flex;
  flex-direction: column-reverse;
  gap: 2rem;
  padding: 2rem 0;
  align-items: center;
}
.hero-text h1 {
  font-size: 2rem;
  color: var(--clr-green-primary);
}
.hero-text p {
  font-size: 1rem;
}
.primary-btn {
  background: var(--clr-green-primary);
  color: var(--clr-white);
}
.hero-image img {
  width: 100%;
  border-radius: 8px;
}
@media (min-width: 768px) {
  .hero {
    flex-direction: row;
    text-align: left;
  }
  .hero-text, .hero-image {
    flex: 1;
  }
}

/* 5. ABOUT */
.about {
  text-align: center;
  padding: 3rem 0;
}
.about h2 {
  font-size: 1.75rem;
  color: var(--clr-blue-light);
  margin-bottom: 1rem;
}

/* 6. FEATURES */
.features {
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  text-align: center;
  padding: 3rem 0;
}
@media (min-width: 600px) {
  .features {
    grid-template-columns: repeat(3, 1fr);
  }
}
.feature h3 {
  font-size: 2rem;
  color: var(--clr-green-primary);
}
.feature p {
  font-size: 0.9rem;
  color: var(--clr-text);
}

/* 7. CTA */
.cta {
  background: var(--clr-blue-light);
  text-align: center;
  padding: 3rem 0;
}
.cta h2 {
  font-size: 1.75rem;
  margin-bottom: 0.5rem;
}
.accent-btn {
  background: var(--clr-green-primary);
  color: var(--clr-white);
}

/* 8. FOOTER */
.footer {
  display: grid;
  gap: 2rem;
  padding: 3rem 0;
  background: var(--clr-green-light);
}
.footer-col h4 {
  margin-bottom: 0.5rem;
  color: var(--clr-text);
}
.footer-col p, .footer-col a {
  font-size: 0.9rem;
  color: var(--clr-text);
  text-decoration: none;
}
.footer .social {
  list-style: none;
  display: flex;
  gap: 1rem;
}
@media (min-width: 600px) {
  .footer {
    grid-template-columns: repeat(3, 1fr);
  }
}
