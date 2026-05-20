<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Drive 5 Ghana Ltd.</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
:root{
  --navy:#0A1628;
  --navy2:#0F1F3D;
  --steel:#1C2E4A;
  --mid:#2D4A6B;
  --accent:#4A8FBF;
  --accent2:#6AAFDF;
  --gold:#C8A96E;
  --gold2:#E8C98E;
  --white:#F5F7FA;
  --offwhite:#E8ECF2;
  --muted:#8A9BB0;
  --text:#D0D8E8;
}
html{scroll-behavior:smooth;}
body{font-family:'DM Sans',sans-serif;background:var(--navy);color:var(--text);overflow-x:hidden;}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:100;display:flex;align-items:center;justify-content:space-between;padding:1.2rem 3rem;background:rgba(10,22,40,0.92);backdrop-filter:blur(12px);border-bottom:1px solid rgba(74,143,191,0.15);}
.nav-logo{font-family:'Cormorant Garamond',serif;font-size:1.35rem;font-weight:700;color:var(--white);letter-spacing:0.03em;}
.nav-logo span{color:var(--gold);}
.nav-links{display:flex;gap:2rem;list-style:none;}
.nav-links a{color:var(--muted);text-decoration:none;font-size:0.85rem;font-weight:500;letter-spacing:0.06em;text-transform:uppercase;transition:color 0.3s;}
.nav-links a:hover{color:var(--gold);}
.nav-cta{background:transparent;border:1px solid var(--gold);color:var(--gold);padding:0.5rem 1.4rem;font-size:0.8rem;font-weight:500;letter-spacing:0.08em;text-transform:uppercase;cursor:pointer;transition:all 0.3s;}
.nav-cta:hover{background:var(--gold);color:var(--navy);}

/* HERO */
.hero{min-height:100vh;display:flex;align-items:center;position:relative;padding:6rem 3rem 4rem;overflow:hidden;}
.hero-bg{position:absolute;inset:0;background:linear-gradient(135deg,var(--navy) 0%,var(--navy2) 50%,var(--steel) 100%);}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(74,143,191,0.04) 1px,transparent 1px),linear-gradient(90deg,rgba(74,143,191,0.04) 1px,transparent 1px);background-size:60px 60px;}
.hero-accent{position:absolute;top:-10%;right:-5%;width:600px;height:600px;border-radius:50%;background:radial-gradient(circle,rgba(74,143,191,0.08) 0%,transparent 70%);pointer-events:none;}
.hero-accent2{position:absolute;bottom:-15%;left:-5%;width:400px;height:400px;border-radius:50%;background:radial-gradient(circle,rgba(200,169,110,0.06) 0%,transparent 70%);pointer-events:none;}
.hero-content{position:relative;max-width:780px;}
.hero-tag{display:inline-flex;align-items:center;gap:0.5rem;background:rgba(74,143,191,0.1);border:1px solid rgba(74,143,191,0.25);color:var(--accent2);padding:0.4rem 1rem;font-size:0.75rem;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:2rem;}
.hero-tag::before{content:'';width:6px;height:6px;border-radius:50%;background:var(--accent2);animation:pulse 2s infinite;}
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.3;}}
h1.hero-title{font-family:'Cormorant Garamond',serif;font-size:clamp(3rem,7vw,5.5rem);font-weight:700;line-height:1.05;color:var(--white);margin-bottom:1.5rem;}
h1.hero-title em{color:var(--gold);font-style:normal;}
.hero-sub{font-size:1.05rem;color:var(--muted);line-height:1.75;max-width:560px;margin-bottom:2.5rem;font-weight:300;}
.hero-btns{display:flex;gap:1rem;flex-wrap:wrap;}
.btn-primary{background:var(--gold);color:var(--navy);padding:0.85rem 2rem;font-size:0.85rem;font-weight:600;letter-spacing:0.06em;text-transform:uppercase;border:none;cursor:pointer;transition:all 0.3s;}
.btn-primary:hover{background:var(--gold2);transform:translateY(-2px);}
.btn-outline{background:transparent;color:var(--white);padding:0.85rem 2rem;font-size:0.85rem;font-weight:500;letter-spacing:0.06em;text-transform:uppercase;border:1px solid rgba(255,255,255,0.25);cursor:pointer;transition:all 0.3s;}
.btn-outline:hover{border-color:var(--white);transform:translateY(-2px);}
.hero-stats{position:absolute;right:3rem;bottom:3rem;display:flex;gap:3rem;}
.stat{text-align:right;}
.stat-num{font-family:'Cormorant Garamond',serif;font-size:2.5rem;font-weight:700;color:var(--white);}
.stat-num span{color:var(--gold);}
.stat-label{font-size:0.72rem;color:var(--muted);letter-spacing:0.1em;text-transform:uppercase;}

/* SECTIONS */
section{padding:6rem 3rem;}
.section-tag{font-size:0.72rem;letter-spacing:0.15em;text-transform:uppercase;color:var(--gold);margin-bottom:0.75rem;}
.section-title{font-family:'Cormorant Garamond',serif;font-size:clamp(2rem,4vw,3rem);font-weight:700;color:var(--white);line-height:1.2;margin-bottom:1rem;}
.section-sub{color:var(--muted);font-size:0.95rem;line-height:1.75;max-width:520px;font-weight:300;}

/* ABOUT */
.about{background:var(--navy2);position:relative;overflow:hidden;}
.about-inner{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center;max-width:1100px;margin:0 auto;}
.about-text .section-sub{max-width:100%;}
.about-visual{position:relative;}
.about-card{background:var(--steel);border:1px solid rgba(74,143,191,0.2);padding:2rem;margin-bottom:1rem;position:relative;overflow:hidden;}
.about-card::before{content:'';position:absolute;left:0;top:0;bottom:0;width:3px;background:var(--gold);}
.about-card h4{font-family:'Cormorant Garamond',serif;font-size:1.15rem;color:var(--white);margin-bottom:0.4rem;padding-left:1rem;}
.about-card p{font-size:0.85rem;color:var(--muted);padding-left:1rem;line-height:1.65;}
.about-badge{display:inline-block;background:rgba(200,169,110,0.1);border:1px solid rgba(200,169,110,0.3);color:var(--gold);font-size:0.75rem;letter-spacing:0.08em;padding:0.35rem 0.9rem;text-transform:uppercase;margin-top:1.5rem;}

/* SERVICES */
.services{background:var(--navy);}
.services-header{text-align:center;max-width:600px;margin:0 auto 4rem;}
.services-header .section-sub{margin:0 auto;}
.services-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5px;background:rgba(74,143,191,0.1);max-width:1100px;margin:0 auto;}
.service-card{background:var(--navy);padding:2.5rem;transition:all 0.3s;cursor:pointer;position:relative;overflow:hidden;}
.service-card::after{content:'';position:absolute;bottom:0;left:0;right:0;height:2px;background:var(--gold);transform:scaleX(0);transition:transform 0.4s;}
.service-card:hover::after{transform:scaleX(1);}
.service-card:hover{background:var(--navy2);}
.service-num{font-family:'Cormorant Garamond',serif;font-size:0.8rem;color:rgba(200,169,110,0.4);letter-spacing:0.1em;margin-bottom:0.5rem;}
.service-card h3{font-family:'Cormorant Garamond',serif;font-size:1.4rem;color:var(--white);margin-bottom:0.75rem;}
.service-card p{font-size:0.83rem;color:var(--muted);line-height:1.7;}

/* PORTFOLIO */
.portfolio{background:var(--navy2);}
.portfolio-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:3rem;max-width:1100px;margin-left:auto;margin-right:auto;}
.portfolio-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;max-width:1100px;margin:0 auto;}
.case-card{background:var(--steel);border:1px solid rgba(74,143,191,0.12);padding:2.5rem;transition:all 0.35s;cursor:pointer;position:relative;}
.case-card:hover{border-color:rgba(200,169,110,0.3);transform:translateY(-4px);}
.case-tag{display:inline-block;background:rgba(74,143,191,0.12);color:var(--accent2);font-size:0.7rem;letter-spacing:0.1em;text-transform:uppercase;padding:0.3rem 0.8rem;margin-bottom:1.25rem;}
.case-card h3{font-family:'Cormorant Garamond',serif;font-size:1.5rem;color:var(--white);margin-bottom:0.75rem;}
.case-card p{font-size:0.85rem;color:var(--muted);line-height:1.7;margin-bottom:1.5rem;}
.case-result{display:flex;gap:1.5rem;}
.case-result-item{text-align:center;}
.case-result-num{font-family:'Cormorant Garamond',serif;font-size:1.6rem;color:var(--gold);}
.case-result-label{font-size:0.68rem;color:var(--muted);text-transform:uppercase;letter-spacing:0.08em;}

/* TEAM */
.team{background:var(--navy);}
.team-header{text-align:center;max-width:600px;margin:0 auto 4rem;}
.team-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1.5rem;max-width:1100px;margin:0 auto;}
.team-card{background:var(--steel);border:1px solid rgba(74,143,191,0.1);padding:2rem 1.5rem;text-align:center;transition:all 0.3s;cursor:pointer;}
.team-card:hover{border-color:rgba(200,169,110,0.25);transform:translateY(-3px);}
.team-avatar{width:72px;height:72px;border-radius:50%;background:linear-gradient(135deg,var(--mid),var(--accent));display:flex;align-items:center;justify-content:center;margin:0 auto 1.25rem;font-family:'Cormorant Garamond',serif;font-size:1.5rem;color:var(--white);font-weight:700;}
.team-card h4{font-family:'Cormorant Garamond',serif;font-size:1.1rem;color:var(--white);margin-bottom:0.25rem;}
.team-role{font-size:0.75rem;color:var(--gold);letter-spacing:0.08em;text-transform:uppercase;margin-bottom:0.75rem;}
.team-bio{font-size:0.78rem;color:var(--muted);line-height:1.6;}

/* CONTACT */
.contact{background:var(--navy2);position:relative;overflow:hidden;}
.contact-inner{display:grid;grid-template-columns:1fr 1fr;gap:5rem;max-width:1100px;margin:0 auto;align-items:start;}
.contact-info{padding-top:0.5rem;}
.contact-detail{display:flex;align-items:flex-start;gap:1rem;margin-bottom:1.75rem;}
.contact-icon{width:40px;height:40px;border:1px solid rgba(74,143,191,0.25);display:flex;align-items:center;justify-content:center;color:var(--accent2);font-size:0.9rem;flex-shrink:0;}
.contact-detail h5{font-size:0.72rem;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);margin-bottom:0.25rem;}
.contact-detail p{font-size:0.9rem;color:var(--text);}
.contact-form{display:flex;flex-direction:column;gap:1rem;}
.form-group{display:flex;flex-direction:column;gap:0.4rem;}
.form-group label{font-size:0.72rem;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);}
.form-group input,.form-group textarea,.form-group select{background:var(--steel);border:1px solid rgba(74,143,191,0.2);color:var(--white);padding:0.8rem 1rem;font-family:'DM Sans',sans-serif;font-size:0.88rem;outline:none;transition:border-color 0.3s;}
.form-group input:focus,.form-group textarea:focus,.form-group select:focus{border-color:var(--accent);}
.form-group textarea{resize:vertical;min-height:120px;}
.form-group select{cursor:pointer;}
.form-group select option{background:var(--steel);}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:1rem;}

/* FOOTER */
footer{background:var(--navy);border-top:1px solid rgba(74,143,191,0.1);padding:3rem;}
.footer-inner{max-width:1100px;margin:0 auto;display:flex;justify-content:space-between;align-items:center;}
.footer-logo{font-family:'Cormorant Garamond',serif;font-size:1.2rem;font-weight:700;color:var(--white);}
.footer-logo span{color:var(--gold);}
.footer-copy{font-size:0.78rem;color:var(--muted);}
.footer-links{display:flex;gap:1.5rem;}
.footer-links a{font-size:0.78rem;color:var(--muted);text-decoration:none;transition:color 0.3s;}
.footer-links a:hover{color:var(--gold);}

/* DIVIDER */
.divider{width:40px;height:2px;background:var(--gold);margin:1.25rem 0 1.5rem;}

/* ANIMATIONS */
.fade-in{opacity:0;transform:translateY(20px);transition:opacity 0.7s,transform 0.7s;}
.fade-in.visible{opacity:1;transform:translateY(0);}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo"><span>D5</span> Ghana Ltd.</div>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Work</a></li>
    <li><a href="#team">Team</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <button class="nav-cta" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Get In Touch</button>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-accent"></div>
  <div class="hero-accent2"></div>
  <div class="hero-content">
    <div class="hero-tag">Ghana's Premier PR Agency</div>
    <h1 class="hero-title">Shaping <em>Narratives.</em><br>Building <em>Legacies.</em></h1>
    <p class="hero-sub">Drive 5 Ghana Ltd. is a full-service public relations and communications agency helping brands across Ghana and West Africa command attention, build trust, and lead their industries.</p>
    <div class="hero-btns">
      <button class="btn-primary" onclick="document.getElementById('services').scrollIntoView({behavior:'smooth'})">Our Services</button>
      <button class="btn-outline" onclick="document.getElementById('portfolio').scrollIntoView({behavior:'smooth'})">View Our Work</button>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat">
      <div class="stat-num">120<span>+</span></div>
      <div class="stat-label">Clients Served</div>
    </div>
    <div class="stat">
      <div class="stat-num">08<span>+</span></div>
      <div class="stat-label">Years Active</div>
    </div>
    <div class="stat">
      <div class="stat-num">15<span>+</span></div>
      <div class="stat-label">Industry Awards</div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-inner">
    <div class="about-text fade-in">
      <div class="section-tag">Who We Are</div>
      <h2 class="section-title">Ghana's Most Trusted Communications Partner</h2>
      <div class="divider"></div>
      <p class="section-sub">Drive 5 Ghana Ltd. was founded on the belief that powerful storytelling transforms brands. We craft communications strategies that resonate deeply with Ghanaian and Pan-African audiences while meeting global standards of excellence.</p>
      <p class="section-sub" style="margin-top:1rem;">Our multidisciplinary team brings together expertise across public relations, media, digital platforms, and strategic communications to deliver measurable impact for every client.</p>
      <span class="about-badge">Accra · Ghana · West Africa</span>
    </div>
    <div class="about-visual fade-in">
      <div class="about-card">
        <h4>Our Mission</h4>
        <p>To amplify authentic voices and build enduring reputations through strategic, culturally intelligent communications that drive real business outcomes.</p>
      </div>
      <div class="about-card">
        <h4>Our Vision</h4>
        <p>To be West Africa's most respected communications agency — setting the standard for ethical, impactful, and innovative PR practice.</p>
      </div>
      <div class="about-card">
        <h4>Our Values</h4>
        <p>Integrity in every engagement. Excellence in every deliverable. Impact in every campaign. These aren't aspirations — they are our daily standard.</p>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div class="services-header fade-in">
    <div class="section-tag">What We Do</div>
    <h2 class="section-title">Comprehensive Communications Services</h2>
    <p class="section-sub">From strategic planning to real-time crisis response, we provide the full spectrum of communications services your brand needs to thrive.</p>
  </div>
  <div class="services-grid">
    <div class="service-card fade-in">
      <div class="service-num">01</div>
      <h3>Public Relations</h3>
      <p>Strategic PR campaigns that shape public perception, build brand equity, and position your organisation as an industry authority across Ghana and West Africa.</p>
    </div>
    <div class="service-card fade-in">
      <div class="service-num">02</div>
      <h3>Media Relations</h3>
      <p>Cultivated relationships with leading Ghanaian and international media houses ensure your story reaches the right audiences through trusted voices.</p>
    </div>
    <div class="service-card fade-in">
      <div class="service-num">03</div>
      <h3>Brand Strategy</h3>
      <p>We help you articulate your brand's identity, define your positioning, and develop a compelling narrative that differentiates you from the competition.</p>
    </div>
    <div class="service-card fade-in">
      <div class="service-num">04</div>
      <h3>Digital Marketing</h3>
      <p>Data-driven digital campaigns spanning social media, content marketing, SEO, and paid advertising — engineered to grow your audience and convert attention into action.</p>
    </div>
    <div class="service-card fade-in">
      <div class="service-num">05</div>
      <h3>Event Management</h3>
      <p>From product launches to corporate conferences and high-profile press events, we design and execute experiences that generate buzz and lasting impressions.</p>
    </div>
    <div class="service-card fade-in">
      <div class="service-num">06</div>
      <h3>Crisis Communication</h3>
      <p>When your reputation is on the line, our rapid-response crisis team provides the strategic counsel and communications support to protect and restore trust.</p>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section class="portfolio" id="portfolio">
  <div class="portfolio-header fade-in">
    <div>
      <div class="section-tag">Our Work</div>
      <h2 class="section-title">Case Studies</h2>
    </div>
    <p style="color:var(--muted);font-size:0.85rem;max-width:300px;text-align:right;">A selection of campaigns we're proud to have delivered for our clients across Ghana.</p>
  </div>
  <div class="portfolio-grid">
    <div class="case-card fade-in">
      <span class="case-tag">Brand Strategy · Media Relations</span>
      <h3>National Bank Rebrand Launch</h3>
      <p>Orchestrated a nationwide communications campaign for a major Ghanaian bank's rebrand, managing media relations, stakeholder engagement, and public messaging across 12 weeks.</p>
      <div class="case-result">
        <div class="case-result-item"><div class="case-result-num">94%</div><div class="case-result-label">Positive Media Coverage</div></div>
        <div class="case-result-item"><div class="case-result-num">3.2M</div><div class="case-result-label">Impressions</div></div>
        <div class="case-result-item"><div class="case-result-num">+40%</div><div class="case-result-label">Brand Recall</div></div>
      </div>
    </div>
    <div class="case-card fade-in">
      <span class="case-tag">Crisis Communication</span>
      <h3>Corporate Crisis Response</h3>
      <p>Provided swift crisis communications support for a leading Accra-based manufacturer facing a product controversy, containing reputational damage and restoring stakeholder confidence within 72 hours.</p>
      <div class="case-result">
        <div class="case-result-item"><div class="case-result-num">72h</div><div class="case-result-label">Response Time</div></div>
        <div class="case-result-item"><div class="case-result-num">85%</div><div class="case-result-label">Sentiment Recovery</div></div>
        <div class="case-result-item"><div class="case-result-num">0</div><div class="case-result-label">Regulatory Actions</div></div>
      </div>
    </div>
    <div class="case-card fade-in">
      <span class="case-tag">Digital Marketing · Event Management</span>
      <h3>Tech Startup Market Entry</h3>
      <p>Supported a West African fintech startup entering the Ghanaian market with an integrated PR and digital strategy, culminating in a high-profile launch event at Accra's leading conference centre.</p>
      <div class="case-result">
        <div class="case-result-item"><div class="case-result-num">500+</div><div class="case-result-label">Event Attendees</div></div>
        <div class="case-result-item"><div class="case-result-num">28</div><div class="case-result-label">Media Features</div></div>
        <div class="case-result-item"><div class="case-result-num">10K+</div><div class="case-result-label">New App Downloads</div></div>
      </div>
    </div>
    <div class="case-card fade-in">
      <span class="case-tag">Public Relations · Brand Strategy</span>
      <h3>NGO Visibility Campaign</h3>
      <p>Developed a six-month PR and advocacy communications strategy for an international NGO operating in Northern Ghana, elevating their profile with donors, government, and the public.</p>
      <div class="case-result">
        <div class="case-result-item"><div class="case-result-num">200%</div><div class="case-result-label">Donor Increase</div></div>
        <div class="case-result-item"><div class="case-result-num">45</div><div class="case-result-label">Media Placements</div></div>
        <div class="case-result-item"><div class="case-result-num">4</div><div class="case-result-label">Gov't Partnerships</div></div>
      </div>
    </div>
  </div>
</section>

<!-- TEAM -->
<section class="team" id="team">
  <div class="team-header fade-in">
    <div class="section-tag">Our People</div>
    <h2 class="section-title">Meet the Team</h2>
    <p class="section-sub" style="margin:0 auto;">A team of seasoned communications professionals united by a passion for storytelling and a commitment to client excellence.</p>
  </div>
  <div class="team-grid">
    <div class="team-card fade-in">
      <div class="team-avatar">AK</div>
      <h4>Ama Kusi</h4>
      <div class="team-role">CEO & Founder</div>
      <p class="team-bio">15+ years in strategic PR and corporate communications across Africa's leading brands.</p>
    </div>
    <div class="team-card fade-in">
      <div class="team-avatar">KO</div>
      <h4>Kwame Osei</h4>
      <div class="team-role">Head of Media Relations</div>
      <p class="team-bio">Former journalist with deep relationships across Ghana's major print, broadcast and digital media.</p>
    </div>
    <div class="team-card fade-in">
      <div class="team-avatar">EA</div>
      <h4>Efua Asante</h4>
      <div class="team-role">Digital Strategy Lead</div>
      <p class="team-bio">Data-driven marketer specialising in social media, content strategy and performance campaigns.</p>
    </div>
    <div class="team-card fade-in">
      <div class="team-avatar">JM</div>
      <h4>Jonas Mensah</h4>
      <div class="team-role">Crisis & Brand Consultant</div>
      <p class="team-bio">Expert in corporate reputation management and crisis communications for regulated industries.</p>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="contact-inner">
    <div class="contact-info fade-in">
      <div class="section-tag">Get In Touch</div>
      <h2 class="section-title">Let's Start a Conversation</h2>
      <div class="divider"></div>
      <p class="section-sub" style="margin-bottom:2.5rem;">Whether you need a full PR strategy, a crisis response team, or a digital campaign — we'd love to hear from you.</p>
      <div class="contact-detail">
        <div class="contact-icon">📍</div>
        <div><h5>Our Office</h5><p>Cantonments, Accra, Ghana</p></div>
      </div>
      <div class="contact-detail">
        <div class="contact-icon">📞</div>
        <div><h5>Phone</h5><p>+233 (0) 30 000 0000</p></div>
      </div>
      <div class="contact-detail">
        <div class="contact-icon">✉️</div>
        <div><h5>Email</h5><p>hello@drive5ghana.com</p></div>
      </div>
    </div>
    <div class="fade-in">
      <div class="contact-form">
        <div class="form-row">
          <div class="form-group">
            <label>First Name</label>
            <input type="text" placeholder="Kwame"/>
          </div>
          <div class="form-group">
            <label>Last Name</label>
            <input type="text" placeholder="Mensah"/>
          </div>
        </div>
        <div class="form-group">
          <label>Email Address</label>
          <input type="email" placeholder="you@company.com"/>
        </div>
        <div class="form-group">
          <label>Company / Organisation</label>
          <input type="text" placeholder="Company Name"/>
        </div>
        <div class="form-group">
          <label>Service of Interest</label>
          <select>
            <option>Public Relations</option>
            <option>Media Relations</option>
            <option>Brand Strategy</option>
            <option>Digital Marketing</option>
            <option>Event Management</option>
            <option>Crisis Communication</option>
            <option>General Enquiry</option>
          </select>
        </div>
        <div class="form-group">
          <label>Message</label>
          <textarea placeholder="Tell us about your project or challenge..."></textarea>
        </div>
        <button class="btn-primary" style="width:100%;padding:1rem;font-size:0.85rem;" onclick="alert('Thank you for your message! The Drive 5 team will be in touch within 24 hours.')">Send Message</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-logo"><span>Drive 5</span> Ghana Ltd.</div>
    <div class="footer-copy">© 2025 Drive 5 Ghana Ltd. All rights reserved.</div>
    <div class="footer-links">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</footer>

<script>
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.1 });
document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
</script>

</body>
</html>
