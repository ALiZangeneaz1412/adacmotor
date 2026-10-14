<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#17191c">
<meta name="description" content="ADAC MOTOR — Premium Motorcycle Gallery & Marketplace. Discover exceptional motorcycles.">
<title>ADAC MOTOR | Premium Motorcycle Gallery</title>
<style>
:root {
  --yellow: #ffd400;
  --bg: #111214;
  --panel: #1b1d20;
  --muted: #a5a7aa;
  --white: #f6f6f3;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--bg);
  color: var(--white);
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.6;
}
a { color: inherit; text-decoration: none; }
.container { width: min(1160px, 90%); margin: auto; }
header {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(17,18,20,.95);
  border-bottom: 1px solid #303236;
  backdrop-filter: blur(12px);
}
.nav {
  min-height: 76px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}
.logo { font-size: 25px; font-weight: 900; letter-spacing: 2px; }
.logo span { color: var(--yellow); }
nav { display: flex; gap: 24px; font-size: 13px; }
nav a:hover { color: var(--yellow); }
.button {
  display: inline-block;
  padding: 12px 19px;
  background: var(--yellow);
  color: #111;
  font-weight: 800;
  border: 0;
  cursor: pointer;
  font-size: 12px;
  letter-spacing: 1px;
}
.hero {
  min-height: 570px;
  display: flex;
  align-items: center;
  background:
    linear-gradient(90deg, rgba(12,13,15,.97) 0%, rgba(12,13,15,.82) 48%, rgba(12,13,15,.18) 100%),
    url('https://images.unsplash.com/photo-1558981806-ec527fa84c39?auto=format&fit=crop&w=1800&q=85') center/cover;
}
.hero-content { max-width: 680px; padding: 90px 0; }
.eyebrow {
  color: var(--yellow);
  font-size: 12px;
  font-weight: 800;
  letter-spacing: 4px;
  text-transform: uppercase;
}
h1 {
  font-size: clamp(42px, 7vw, 82px);
  line-height: 1.02;
  margin: 20px 0;
  letter-spacing: -2px;
}
h1 span { color: var(--yellow); }
.hero p { max-width: 490px; color: #d0d0d0; margin-bottom: 28px; }
.stats {
  display: flex;
  flex-wrap: wrap;
  gap: 35px;
  margin-top: 45px;
}
.stat strong { display: block; font-size: 25px; }
.stat small { color: var(--muted); font-size: 11px; letter-spacing: 1px; }
section { padding: 85px 0; }
.section-head {
  display: flex;
  justify-content: space-between;
  align-items: end;
  gap: 20px;
  margin-bottom: 35px;
}
h2 { font-size: clamp(28px, 4vw, 43px); line-height: 1.2; }
.section-head p { color: var(--muted); font-size: 13px; margin-top: 8px; }
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 22px;
}
.card {
  background: var(--panel);
  border: 1px solid #303236;
  overflow: hidden;
  transition: transform .25s, border-color .25s;
}
.card:hover { transform: translateY(-5px); border-color: var(--yellow); }
.card img { width: 100%; height: 220px; object-fit: cover; display: block; }
.card-body { padding: 21px; }
.tag {
  display: inline-block;
  font-size: 10px;
  color: var(--yellow);
  border: 1px solid #625819;
  padding: 4px 8px;
  letter-spacing: 1px;
}
.card h3 { font-size: 20px; margin: 13px 0 5px; }
.card p { color: var(--muted); font-size: 12px; }
.card-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  margin-top: 20px;
  padding-top: 16px;
  border-top: 1px solid #34363a;
}
.price { color: var(--yellow); font-size: 13px; font-weight: bold; }
.details { font-size: 11px; font-weight: bold; }
.about {
  background: #191a1d;
  border-top: 1px solid #303236;
  border-bottom: 1px solid #303236;
}
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 55px;
}
.about-image img { width: 100%; display: block; min-height: 300px; object-fit: cover; }
.about-copy p { color: #b9b9bb; margin: 20px 0; }
.features { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 25px; }
.feature { padding: 15px; border-left: 3px solid var(--yellow); background: #222427; }
.feature strong { display: block; font-size: 13px; }
.feature small { color: var(--muted); font-size: 11px; }
.contact-box {
  background: var(--yellow);
  color: #111;
  padding: 45px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 25px;
}
.contact-box p { margin-top: 8px; font-size: 13px; }
.contact-box .button { background: #111; color: white; }
footer { padding: 30px 0; color: var(--muted); font-size: 11px; }
.footer-row { display: flex; justify-content: space-between; gap: 20px; flex-wrap: wrap; }
footer strong { color: white; }
@media(max-width: 800px) {
  nav { gap: 12px; }
  .nav { flex-wrap: wrap; padding: 15px 0; }
  .grid { grid-template-columns: repeat(2, 1fr); }
  .about-grid { grid-template-columns: 1fr; }
}
@media(max-width: 540px) {
  nav { width: 100%; justify-content: space-between; order: 3; }
  .nav > .button { padding: 9px 11px; }
  .grid { grid-template-columns: 1fr; }
  .hero { min-height: 520px; }
  .section-head { align-items: start; flex-direction: column; }
  .contact-box { padding: 28px; flex-direction: column; align-items: start; }
  .stats { gap: 22px; }
}
</style>
</head>
<body>

<header>
  <div class="container nav">
    <a class="logo" href="#home">ADAC<span>.</span>MOTOR</a>
    <nav>
      <a href="#home">HOME</a>
      <a href="#inventory">MOTORCYCLES</a>
      <a href="#about">ABOUT</a>
      <a href="#contact">CONTACT</a>
    </nav>
    <a class="button" href="#inventory">EXPLORE BIKES ↗</a>
  </div>
</header>

<main>
  <section class="hero" id="home">
    <div class="container">
      <div class="hero-content">
        <div class="eyebrow">Premium Motorcycle Gallery</div>
        <h1>RIDE BEYOND<br>THE <span>ORDINARY.</span></h1>
        <p>
          Exceptional motorcycles. Unmistakable character.
          Discover your next machine at ADAC MOTOR.
        </p>
        <a class="button" href="#inventory">DISCOVER THE COLLECTION ↗</a>
        <div class="stats">
          <div class="stat"><strong>01</strong><small>PREMIUM EXPERIENCE</small></div>
          <div class="stat"><strong>100%</strong><small>PASSION FOR RIDING</small></div>
          <div class="stat"><strong>ADAC</strong><small>BUILT FOR RIDERS</small></div>
        </div>
      </div>
    </div>
  </section>

  <section id="inventory">
    <div class="container">
      <div class="section-head">
        <div>
          <div class="eyebrow">Selected Machines</div>
          <h2>THE COLLECTION<span style="color:var(--yellow)">.</span></h2>
          <p>A preview of the machines that inspire us.</p>
        </div>
        <span class="tag">SPORT · STREET · PERFORMANCE</span>
      </div>

      <div class="grid">
        <article class="card">
          <img src="https://images.unsplash.com/photo-1568772585407-9361f9bf3a87?auto=format&fit=crop&w=900&q=80" alt="Sport motorcycle">
          <div class="card-body">
            <span class="tag">SUPERSPORT</span>
            <h3>Sport Series</h3>
            <p>Sharp design. Pure adrenaline. Track-inspired spirit.</p>
            <div class="card-bottom">
              <span class="price">CONTACT FOR PRICE</span>
              <a class="details" href="#contact">ENQUIRE ↗</a>
            </div>
          </div>
        </article>

        <article class="card">
          <img src="https://images.unsplash.com/photo-1558981806-ec527fa84c39?auto=format&fit=crop&w=900&q=80" alt="Performance motorcycle">
          <div class="card-body">
            <span class="tag">PERFORMANCE</span>
            <h3>Performance Series</h3>
            <p>Powerful presence for riders who demand more.</p>
            <div class="card-bottom">
              <span class="price">CONTACT FOR PRICE</span>
              <a class="details" href="#contact">ENQUIRE ↗</a>
            </div>
          </div>
        </article>

        <article class="card">
          <img src="https://images.unsplash.com/photo-1449426468159-d96dbf08f19f?auto=format&fit=crop&w=900&q=80" alt="Motorcycle on the road">
          <div class="card-body">
            <span class="tag">STREET</span>
            <h3>Street Series</h3>
            <p>Everyday freedom with a distinctive attitude.</p>
            <div class="card-bottom">
              <span class="price">CONTACT FOR PRICE</span>
              <a class="details" href="#contact">ENQUIRE ↗</a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section class="about" id="about">
    <div class="container about-grid">
      <div class="about-image">
        <img src="https://images.unsplash.com/photo-1558981403-c5f9899a28bc?auto=format&fit=crop&w=1100&q=85" alt="Motorcycle engineering and design">
      </div>
      <div class="about-copy">
        <div class="eyebrow">The ADAC Philosophy</div>
        <h2>MORE THAN A<br><span style="color:var(--yellow)">MOTORCYCLE.</span></h2>
        <p>
          ADAC MOTOR is built around a passion for motorcycles,
          distinctive design and the excitement of finding the right machine.
          Every ride starts with the right choice.
        </p>
        <div class="features">
          <div class="feature"><strong>SELECTED MACHINES</strong><small>Quality over quantity</small></div>
          <div class="feature"><strong>RIDER FOCUSED</strong><small>Made for enthusiasts</small></div>
          <div class="feature"><strong>PERSONAL SERVICE</strong><small>A direct experience</small></div>
          <div class="feature"><strong>BUILT ON PASSION</strong><small>Driven by motorcycles</small></div>
        </div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <div class="contact-box">
        <div>
          <h2>YOUR NEXT RIDE<br>STARTS HERE.</h2>
          <p>Interested in a motorcycle? Get in touch with ADAC MOTOR.</p>
        </div>
        <a class="button" href="mailto:adacmotor@example.com?subject=Motorcycle%20Enquiry">CONTACT THE GALLERY ↗</a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="container footer-row">
    <div><strong>ADAC MOTOR</strong> — Premium Motorcycle Gallery</div>
    <div>© <span id="year"></span> ADAC MOTOR. ALL RIGHTS RESERVED.</div>
  </div>
</footer>

<script>
document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>
