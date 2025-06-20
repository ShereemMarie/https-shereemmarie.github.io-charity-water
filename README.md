/* style.css */
/* 1. Base & Reset */
:root {
  --clr-primary: #00a6fb;
  --clr-accent:  #f08f5f;
  --clr-dark:    #222;
  --clr-light:   #f4f4f4;
  --fw-regular:  400;
  --fw-bold:     600;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  font-size: 16px;
  scroll-behavior: smooth;
}
body {
  font-family: 'Montserrat', sans-serif;
  line-height: 1.6;
  color: #333;
  background-color: #fff;
}

/* 2. Utility */
.container {
  width: min(90%, 1200px);
  margin: 0 auto;
}
h1, h2, h3, h4 {
  font-weight: var(--fw-bold);
}
p {
  margin-top: 0.5rem;
}

/* 3. Typography (responsive with clamp) */
h1 {
  font-size: clamp(2rem, 5vw + 1rem, 4rem);
  margin-bottom: 1rem;
}
h2 {
  font-size: clamp(1.5rem, 4vw + 1rem, 2.5rem);
  margin-bottom: 0.75rem;
}
h3 {
  font-size: clamp(1.25rem, 3vw + 0.5rem, 2rem);
  margin-bottom: 0.5rem;
}
p, ul, a {
  font-size: clamp(0.9rem, 2vw + 0.2rem, 1.1rem);
}

/* 4. Buttons */
.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-weight: var(--fw-bold);
  transition: background 0.2s ease;
}
.primary-btn {
  background-color: var(--clr-primary);
  color: #fff;
}
.primary-btn:hover,
.accent-btn:hover {
  opacity: 0.9;
}
.accent-btn {
  background-color: var(--clr-accent);
  color: #fff;
}

/* 5. Hero */
header.hero {
  role: banner;
  display: grid;
  gap: 1rem;
  padding: 2rem 0;
  align-items: center;
  text-align: center;
}
.hero-content {
  z-index: 1;
}
.hero-image img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 0.5rem;
}
@media (min-width: 768px) {
  header.hero {
    grid-template-columns: 1fr 1fr;
    text-align: left;
  }
}

/* 6. About */
section.about {
  padding: 3rem 0;
}
section.about h2 {
  text-align: center;
}

/* 7. Features */
.features {
  background: var(--clr-light);
  padding: 2rem 0;
}
.features-grid {
  display: grid;
  gap: 2rem;
  text-align: center;
}
@media (min-width: 600px) {
  .features-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
.feature h3 {
  color: var(--clr-primary);
}

/* 8. CTA */
section.cta {
  role: region;
  aria-labelledby: donate;
  background: var(--clr-dark);
  color: #fff;
  text-align: center;
  padding: 3rem 0;
}

/* 9. Footer */
footer {
  background: var(--clr-dark);
  color: #fff;
  padding: 2rem 0;
  font-size: 0.9rem;
}
.footer-grid {
  display: grid;
  gap: 2rem;
}
@media (min-width: 600px) {
  .footer-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
.footer-grid a {
  color: #fff;
  text-decoration: none;
}
.footer-bottom {
  border-top: 1px solid #444;
  text-align: center;
  margin-top: 1rem;
  padding-top: 1rem;
}
# .github/workflows/deploy.yml
name: CI/CD to GitHub Pages

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v3
/* style.css */
/* 1. Color Palette & Typography Variables */
:root {
  /* Primary palette */
  --clr-blue-light:  #a0e7e5;
  --clr-green-light: #b4f8c8;
  --clr-primary:     #00a6fb;
  --clr-accent:      #f08f5f;
  --clr-dark:        #222;
  --clr-light:       #f4f4f4;

  /* Font weights */
  --fw-regular: 400;
  --fw-bold:    600;
}

/* 2. Reset & Base */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  font-size: 16px;
  scroll-behavior: smooth;
}
body {
  font-family: 'Montserrat', sans-serif;
  color: var(--clr-dark);
  background: var(--clr-light);
  line-height: 1.6;
}

/* 3. Utility */
.container {
  width: min(90%, 1200px);
  margin: 0 auto;
}
h1, h2, h3, h4 {
  font-weight: var(--fw-bold);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
p, li {
  margin-top: 0.5rem;
}

/* 4. Responsive Typography */
h1 {
  color: var(--clr-green-light);
  font-size: clamp(2.5rem, 6vw + 1rem, 5rem);
  text-shadow: 2px 2px var(--clr-blue-light);
  margin-bottom: 1rem;
}
h2 {
  color: var(--clr-primary);
  font-size: clamp(1.75rem, 4.5vw + 1rem, 3rem);
  margin-bottom: 0.75rem;
}
h3 {
  color: var(--clr-blue-light);
  font-size: clamp(1.25rem, 3vw + 0.5rem, 2.5rem);
  margin-bottom: 0.5rem;
}
p, a, button {
  font-size: clamp(0.9rem, 2vw + 0.2rem, 1.1rem);
}

/* 5. Buttons */
.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-weight: var(--fw-bold);
  transition: opacity 0.2s;
}
.primary-btn {
  background-color: var(--clr-blue-light);
  color: var(--clr-dark);
}
.accent-btn {
  background-color: var(--clr-green-light);
  color: var(--clr-dark);
}
.btn:hover {
  opacity: 0.9;
}

/* 6. Hero */
header.hero {
  role: banner;
  display: grid;
  gap: 1rem;
  padding: 3rem 0;
  align-items: center;
  text-align: center;
  background: linear-gradient(135deg, var(--clr-green-light), var(--clr-blue-light));
}
.hero-content h1,
.hero-content p {
  text-shadow: 1px 1px rgba(0,0,0,0.1);
}
.hero-image img {
  width: 100%;
  height: auto;
  border-radius: 0.5rem;
}
@media (min-width: 768px) {
  header.hero {
    grid-template-columns: 1fr 1fr;
    text-align: left;
  }
}

/* 7. About */
section.about {
  padding: 4rem 0;
  background: white;
}
section.about h2 {
  text-align: center;
  color: var(--clr-primary);
}

/* 8. Features */
.features {
  background: var(--clr-light);
  padding: 3rem 0;
}
.features-grid {
  display: grid;
  gap: 2rem;
  text-align: center;
}
@media (min-width: 600px) {
  .features-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
.feature h3 {
  font-size: 2rem;
}

/* 9. CTA */
section.cta {
  role: region;
  aria-labelledby: donate;
  background: var(--clr-primary);
  color: #fff;
  text-align: center;
  padding: 3rem 0;
}

/* 10. Footer */
footer {
  background: var(--clr-dark);
  color: #fff;
  padding: 3rem 0 1rem;
}
.footer-grid {
  display: grid;
  gap: 2rem;
  text-align: left;
}
@media (min-width: 600px) {
  .footer-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
.footer-grid a {
  color: var(--clr-light);
  text-decoration: none;
}
.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.2);
  text-align: center;
  margin-top: 1rem;
  padding-top: 1rem;
}
