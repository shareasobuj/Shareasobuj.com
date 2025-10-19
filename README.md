# Shareasobuj.com
<!--
File: sharesasobuj_portfolio.html
Title: SHAREA SOBUJ SHISHIR — Front-end Developer Portfolio

Usage & Deployment Notes (read before uploading):
1) This is a single-file static website (HTML + internal CSS + JS).
2) To publish with FREE hosting without GitHub, you can use providers like:
   - InfinityFree (https://infinityfree.net) -> upload this file to /htdocs via File Manager or FTP
   - 000webhost (https://www.000webhost.com) -> upload index.html via File Manager
   - Neocities (https://neocities.org) -> create site and paste HTML
3) For a free domain: Freenom may provide free domains (.tk, .ml, .ga, .cf, .gq) — register and point to your hosting's nameservers.
4) If you want the exact domain sharesasobuj.com you'll need to buy it (Namecheap, Porkbun, etc.) and then point its DNS to your host.
5) Contact form: This file opens the user's mail client with a prefilled email using mailto. If you want a server-based form, consider Formspree or Getform and replace the JS submit handler.

Edit the content below (name, projects, links) before uploading.
-->

<html lang="bn">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>SHAREA SOBUJ SHISHIR — Front-end Developer | sharesasobuj.com</title>
  <meta name="description" content="SHAREA SOBUJ SHISHIR — Front-end Web Developer. Portfolio showcasing projects, skills, and contact information.">
  <meta name="author" content="SHAREA SOBUJ SHISHIR">

  <!-- Favicon (simple) -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>💻</text></svg>">

  <style>
    /* Reset & base */
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#94a3b8; --accent:#06b6d4; --glass:rgba(255,255,255,0.03);
      --maxw:1100px;
      color-scheme: dark;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Noto Sans', 'Helvetica Neue', Arial; background:linear-gradient(180deg,#071029 0%, #071726 100%); color:#e6eef6; -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    a{color:var(--accent); text-decoration:none}
    .container{max-width:var(--maxw); margin:0 auto; padding:28px}

    /* Header / Nav */
    header{display:flex; align-items:center; justify-content:space-between; gap:16px; margin-bottom:28px}
    .brand{display:flex; align-items:center; gap:12px}
    .logo{width:52px; height:52px; display:inline-grid; place-items:center; background:linear-gradient(135deg,#06b6d4,#3b82f6); border-radius:12px; font-weight:700}
    .brand h1{font-size:18px; margin:0}
    nav{display:flex; gap:12px; align-items:center}
    .btn{padding:10px 14px; border-radius:10px; background:var(--glass); border:1px solid rgba(255,255,255,0.04); cursor:pointer}

    /* Hero */
    .hero{display:grid; grid-template-columns:1fr 360px; gap:28px; align-items:center; margin-bottom:32px}
    .hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); padding:28px; border-radius:16px; box-shadow:0 6px 24px rgba(2,6,23,0.6)}
    .hero h2{font-size:28px; margin:0 0 8px}
    .hero p.lead{color:var(--muted); margin:0 0 18px}
    .cta{display:flex; gap:12px}
    .primary{background:linear-gradient(90deg,var(--accent),#7c3aed); padding:12px 16px; border-radius:10px; color:#021026; font-weight:600}

    /* Quick skills */
    .skills-row{display:flex; gap:10px; flex-wrap:wrap}
    .chip{padding:8px 10px; border-radius:999px; background:rgba(255,255,255,0.03); border:1px solid rgba(255,255,255,0.02); color:var(--muted); font-size:13px}

    /* Right column card */
    .profile{padding:18px; border-radius:12px; background:linear-gradient(180deg, rgba(255,255,255,0.015), transparent);}
    .avatar{width:100%; border-radius:10px; height:220px; object-fit:cover; background:linear-gradient(180deg,#0ea5a9,#7c3aed); display:grid; place-items:center; font-size:48px}
    .meta{margin-top:12px}
    .meta strong{display:block}

    /* Sections */
    section{margin-bottom:28px}
    h3{margin:0 0 12px}
    .cards{display:grid; grid-template-columns:repeat(3,1fr); gap:14px}
    .card{background:var(--card); padding:16px; border-radius:12px; border:1px solid rgba(255,255,255,0.02)}
    .card h4{margin:0 0 8px}
    .muted{color:var(--muted); font-size:14px}

    /* Projects list */
    .project{display:flex; gap:14px; align-items:flex-start}
    .thumb{width:110px; height:70px; border-radius:8px; background:linear-gradient(90deg,#06b6d4,#7c3aed); display:grid; place-items:center; color:#021026; font-weight:700}

    /* Contact */
    form{display:grid; gap:8px}
    input,textarea{background:transparent; border:1px solid rgba(255,255,255,0.05); padding:10px; border-radius:8px; color:inherit}
    textarea{min-height:120px}

    footer{padding:18px 0; color:var(--muted); text-align:center}

    /* Responsive */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      .cards{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:600px){
      .cards{grid-template-columns:1fr}
      header{flex-direction:column; align-items:flex-start}
    }

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">SS</div>
        <div>
          <h1>sharesasobuj.com</h1>
          <div class="muted">SHAREA SOBUJ SHISHIR — Front-end Web Developer</div>
        </div>
      </div>
      <nav>
        <a class="btn" href="#projects">Projects</a>
        <a class="btn" href="#skills">Skills</a>
        <a class="btn" href="#contact">Contact</a>
        <a class="btn" href="#" onclick="downloadResume()">Download CV</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-card">
          <h2>হ্যালো — আমি SHAREA SOBUJ SHISHIR</h2>
          <p class="lead">আমি একজন ফ্রন্ট-এন্ড ওয়েব ডেভেলপার। আমি responsive, accessible এবং দ্রুত লোডিং ওয়েবসাইট বানাই। আমার কাজের লক্ষ্য — ব্যবহারকারীর জন্য ক্লিয়ার, মসৃণ ও কার্যকর UI তৈরি করা।</p>
          <div class="skills-row" style="margin-bottom:18px">
            <div class="chip">HTML</div>
            <div class="chip">CSS</div>
            <div class="chip">JavaScript</div>
            <div class="chip">Responsive Design</div>
            <div class="chip">React (Basic)</div>
            <div class="chip">Bootstrap / Tailwind</div>
          </div>

          <div class="cta">
            <a class="primary" href="#contact">Hire Me</a>
            <a class="btn" href="#projects">See Projects</a>
          </div>

          <div style="margin-top:18px; color:var(--muted); font-size:14px">Location: Bangladesh · Email: <a href="mailto:shareasobuj@example.com">shareasobuj@example.com</a></div>
        </div>

        <aside class="profile">
          <div class="avatar">SS</div>
          <div class="meta">
            <strong>SHAREA SOBUJ SHISHIR</strong>
            <div class="muted">Front-end Web Developer</div>
            <div style="margin-top:8px" class="muted">I build fast, responsive web apps and attractive UI interfaces. I enjoy turning ideas into real projects.</div>
          </div>
        </aside>
      </section>

      <section id="skills">
        <h3>Skills & Tools</h3>
        <div class="cards">
          <div class="card">
            <h4>Front-end</h4>
            <div class="muted">HTML, CSS, JavaScript, Responsive Layouts, Accessibility</div>
          </div>
          <div class="card">
            <h4>Frameworks</h4>
            <div class="muted">React, Tailwind CSS, Bootstrap</div>
          </div>
          <div class="card">
            <h4>Tools</h4>
            <div class="muted">VS Code, Chrome DevTools, Git (local), Figma (basic)</div>
          </div>
        </div>
      </section>

      <section id="projects">
        <h3>Selected Projects</h3>
        <div style="display:grid;gap:12px">

          <article class="card project">
            <div class="thumb">P1</div>
            <div>
              <h4>Portfolio Template</h4>
              <div class="muted">A clean, responsive portfolio template built with HTML, CSS and vanilla JS. Features: light/dark theme toggle, smooth scroll, and responsive grid for projects.</div>
              <div style="margin-top:8px"><a href="#">Live demo</a> · <a href="#">Source</a></div>
            </div>
          </article>

          <article class="card project">
            <div class="thumb">P2</div>
            <div>
              <h4>E-commerce UI (Mock)</h4>
              <div class="muted">Product listing and product details UI focusing on clean design and mobile-first approach.</div>
              <div style="margin-top:8px"><a href="#">Live demo</a> · <a href="#">Source</a></div>
            </div>
          </article>

          <article class="card project">
            <div class="thumb">P3</div>
            <div>
              <h4>Small Business Site</h4>
              <div class="muted">Landing page + contact form for a local business with responsive hero and testimonial section.</div>
              <div style="margin-top:8px"><a href="#">Live demo</a> · <a href="#">Source</a></div>
            </div>
          </article>

        </div>
      </section>

      <section id="contact">
        <h3>Contact Me</h3>
        <div class="card">
          <form id="contactForm" onsubmit="submitForm(event)">
            <input id="name" type="text" placeholder="Your name" required>
            <input id="email" type="email" placeholder="Your email" required>
            <input id="subject" type="text" placeholder="Subject" required>
            <textarea id="message" placeholder="Your message" required></textarea>
            <div style="display:flex; gap:10px; margin-top:8px">
              <button class="primary" type="submit">Send Message</button>
              <button type="button" class="btn" onclick="copyEmail()">Copy Email</button>
            </div>
          </form>
          <div id="formStatus" style="margin-top:10px; color:var(--muted)"></div>
        </div>
      </section>

    </main>

    <footer>
      © <span id="year"></span> SHAREA SOBUJ SHISHIR — sharesasobuj.com · Built with ❤️
    </footer>

  </div>

  <script>
    // Basic interactive JS
    document.getElementById('year').textContent = new Date().getFullYear();

    function submitForm(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const subject = document.getElementById('subject').value.trim();
      const message = document.getElementById('message').value.trim();

      if(!name || !email || !subject || !message){
        updateStatus('Please fill all fields');
        return;
      }

      // Mailto fallback — opens user's mail client
      const mailto = `mailto:shareasobuj@example.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent('Name: '+name+'\nEmail: '+email+'\n\n'+message)}`;
      window.location.href = mailto;
      updateStatus('Opening your mail client...');
    }

    function updateStatus(text){
      document.getElementById('formStatus').textContent = text;
    }

    function copyEmail(){
      navigator.clipboard?.writeText('shareasobuj@example.com').then(()=>{
        updateStatus('Email copied to clipboard');
      }).catch(()=>{
        updateStatus('Copy failed — please copy manually: shareasobuj@example.com');
      })
    }

    function downloadResume(){
      // Replace with real resume link if you upload one
      const dummy = 'data:text/plain;charset=utf-8,' + encodeURIComponent('SHAREA SOBUJ SHISHIR\nFront-end Web Developer\n(Replace this with your real CV file)');
      const a = document.createElement('a'); a.href = dummy; a.download = 'SHAREA_SOBUJ_SHISHIR_CV.txt'; document.body.appendChild(a); a.click(); a.remove();
    }

  </script>
