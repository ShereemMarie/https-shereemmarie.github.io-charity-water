1. Create & Push Your GitHub Repo
bash
# 1. On GitHub.com, create a new public repo named "Shereemmarie-charity-water"
#    Don’t initialize with README— we’ll add it locally.
git clone git@github.com:YOUR-USERNAME/Shereemarie-charity-water.git
cd Shereemarie-charity-water

# 2. Create your files
touch index.html styles.css README.md

# 3. Add, commit, and push
git add .
git commit -m "Initial commit: landing page for charity: water"
git push origin main
> Enable Pages: In your repo’s Settings → Pages → Source: main branch → save. > Your site will be live at https://YOUR-USERNAME.github.io/Shereemarie-charity-water/

2. Repository Structure
Shereemarie-charity-water/
├── index.html
├── styles.css
└── README.md
3. index.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>charity: water | Transforms lives one drop at a time</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&family=Lora:wght@400&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <!-- Hero -->
  <header class="hero">
    <div class="overlay"></div>
    <div class="hero-content">
      <img src="https://www.charitywater.org/assets/logo.svg" alt="charity: water logo" class="logo">
      <h1>Transforms lives one drop at a time</h1>
      <p>Join us in bringing clean, safe water to communities around the globe. Your support creates hope, health, and opportunity.</p>
      <a href="#donate" class="btn">Donate Now – Every Drop Counts</a>
    </div>
  </header>

  <!-- Impact Info -->
  <section id="why" class="info-section">
    <h2>Why Clean Water Matters</h2>
    <div class="info-grid">
      <div class="info-card">
        <h3>Health</h3>
        <p>Clean water reduces diseases and nurtures healthier communities.</p>
      </div>
      <div class="info-card">
        <h3>Education</h3>
        <p>Reliable water empowers children to learn and grow.</p>
      </div>
      <div class="info-card">
        <h3>Community</h3>
        <p>Water access unites people and sparks lasting progress.</p>
      </div>
    </div>
  </section>

  <!-- Gallery -->
  <section id="gallery" class="gallery-section">
    <h2>Community in Action</h2>
    <div class="gallery-grid">
      <img src="https://source.unsplash.com/400x300/?before,drought" alt="Before drought">
      <img src="https://source.unsplash.com/400x300/?after,water" alt="After clean water">
      <img src="https://source.unsplash.com/400x300/?volunteers,water" alt="Volunteers">
      <img src="https://source.unsplash.com/400x300/?leaf,water" alt="Water droplets">
      <img src="https://source.unsplash.com/400x300/?well,community" alt="Well celebration">
    </div>
  </section>

  <!-- Testimonials -->
  <section id="stories" class="testimonials-section">
    <h2>Success Stories</h2>
    <blockquote>
      “Our village now has safe water daily—our children are healthier and happier.”<br>
      <cite>– Community Leader</cite>
    </blockquote>
    <div class="counter">Over 25,000 lives transformed</div>
  </section>

  <!-- CTA -->
  <section id="donate" class="donate-section">
    <h2>Make a Difference Today</h2>
    <a href="https://www.charitywater.org/donate" class="btn">Donate Now – Every Drop Counts</a>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 charity: water. All rights reserved.</p>
  </footer>
</body>
</html>
4. styles.css
css
/* Reset & Base */
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family:'Lora', serif; background:#fff; color:#333; }

/* Brand Colors & Typography */
:root {
  --deep-blue: #005B96;
  --fresh-green: #3CB371;
  --soft-white: #FFFFFF;
  --header-font: 'Montserrat', sans-serif;
  --body-font: 'Lora', serif;
}
h1,h2,h3 { font-family: var(--header-font); margin-bottom: .5em; }
p,blockquote { font-family: var(--body-font); line-height: 1.6; }

/* Hero */
.hero {
  position: relative; height:100vh;
  background: url('https://source.unsplash.com/1600x900/?community,water') center/cover no-repeat;
  display:flex; align-items:center; justify-content:center; text-align:center;
  color: var(--soft-white);
}
.hero .overlay {
  position:absolute; inset:0; background: rgba(0,0,0,.4);
}
.hero-content {
  position:relative; max-width:600px; padding:0 1em;
}
.logo { max-width:120px; margin-bottom:1em; }
.hero h1 { font-size:2.5rem; }
.hero p { margin:1em 0; font-size:1.1rem; }
.btn {
  display:inline-block; background: var(--fresh-green); color:#fff;
  padding:.75em 1.5em; border-radius:5px; transition:.3s;
}
.btn:hover { background: darken(var(--fresh-green),10%); }

/* Info Section */
.info-section { padding:4em 1em; background:#f5f5f5; }
.info-section h2 { color: var(--deep-blue); }
.info-grid {
  display:grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr)); gap:1.5em;
  margin-top:2em;
}
.info-card {
  background:#fff; padding:1.5em; border-radius:5px;
  box-shadow:0 2px 6px rgba(0,0,0,.1);
}
.info-card h3 { color: var(--deep-blue); }

/* Gallery */
.gallery-section { padding:4em 1em; }
.gallery-grid {
  display:grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr)); gap:1em;
}
.gallery-grid img {
  width:100%; height:150px; object-fit:cover; border-radius:5px;
  transition: transform .3s;
}
.gallery-grid img:hover { transform: scale(1.05); }

/* Testimonials */
.testimonials-section { padding:4em 1em; background:#f5f5f5; text-align:center; }
.testimonials-section blockquote {
  font-style:italic; margin-bottom:1em; position:relative;
}
.testimonials-section cite { display:block; font-weight:bold; margin-top:.5em; }
.counter {
  font-size:1.5rem; color: var(--deep-blue); margin-top:1em;
}

/* Donate CTA */
.donate-section { padding:4em 1em; text-align:center; }
.donate-section h2 { margin-bottom:1em; color: var(--deep-blue); }

/* Footer */
footer {
  background: var(--deep-blue); color:#fff; text-align:center; padding:1em 0;
}

/* Responsive */
@media(max-width:600px){
  .hero h1 { font-size:2rem; }
}
5. README.md
markdown
# Shereemarie-charity-water  

A modern, clean landing page for [charity: water](https://www.charitywater.org/) built and hosted on GitHub Pages.

## Features  
- **Headline & Subheadline:** “Transforms lives one drop at a time”  
- **Brand Palette:** Deep Blue, Fresh Green, Soft White  
- **Typography:** Montserrat Bold & Lora Regular  
- **Dynamic Hero** with full-screen image + overlay  
- **Impact Info, Gallery, Testimonials** and **strong CTA**  

## How to run locally  
1. `git clone https://github.com/YOUR-USERNAME/Shereemarie-charity-water.git`  
2. `cd Shereemarie-charity-water`  
3. Open `index.html` in your browser  

## License  
MIT © YOUR NAME
Once you push these files, visit

https://YOUR-USERNAME.github.io/Shereemarie-charity-water
