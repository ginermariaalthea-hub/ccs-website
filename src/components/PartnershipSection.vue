
<script setup>
const news = [
  {
    title: 'Victory for Nathan Zech C. Pugales',
    date: 'Latest News',
    description:
      'A well-earned victory for Nathan Zech C. Pugales, who emerged as the CHAMPION of the MC3D Prime HO Cebu Grand Opening LAN Tournament — TEKKEN Tournament!',
    image: '/tek.jpg'
  },
  {
    title: '𝗔 𝗣𝗟𝗔𝗖𝗘 𝗔𝗠𝗢𝗡𝗚 𝗧𝗛𝗘 𝗧𝗢𝗣 𝟲𝟬!',
    date: '2026',
    description:
      'Making their mark on the national stage, BS Computer Science 3 students Abegail Lentija, Fred Allen Dimo, and John Reynelle Delfin have secured a spot among the Top 60 teams out of 200+ participants in the Enactus Philippines National Competition 2026 – Early-Stage Project Track! With the guidance of their adviser, Ma’am Roda Katrina C. Eregia, the team continues to demonstrate the potential of young innovators to turn ideas into meaningful impact.',
    image: '/60.jpg'
  },
  {
    title: '3 Peat Champs',
    date: 'October 2, 2026',
    description:
      'The CCS Warriors brought the heat to the streets of Central Philippine University on October 2, 2026, during the University Week and Centralian Festival 2026 Street Dance Competition, delivering a performance packed with energy, creativity, and teamwork!',
    image: '/sdance.jpg'
  }
]
</script>

<template>
  <div>
    <!-- VISION AND MISSION -->
    <section id="about" class="about section">
      <div class="container about-grid">

        <div class="vision-content">
          <p class="eyebrow">OUR PURPOSE</p>

          <h2>Our <span>Vision</span></h2>

          <p class="about-copy">
            The College of Computer Studies is founded on the
            vision of academic excellence in Information Technology
            Education and responsive to the needs of the total person
            and the world.
          </p>
        </div>

        <div class="mission-content">
          <p class="eyebrow">OUR COMMITMENT</p>

          <h2>Our <span>Mission</span></h2>

          <p class="about-copy">
            A College of the future with a mission to educate students
            with the Christian principles and practices of computer
            studies, preparing them to advance studies, careers in
            software development, computing systems technology,
            information management, and for a lifetime learning.
          </p>
        </div>

      </div>
    </section>

    <!-- NEWS AND UPDATES -->
    <section id="news" class="news section">
      <div class="container">

        <div class="section-heading">
          <p class="eyebrow">CAMPUS LIFE</p>

          <h2>News & <span>Updates</span></h2>

          <p>
            Be updated with college activities and achievements.
          </p>
        </div>

        <div class="news-grid">
          <article
            v-for="item in news"
            :key="item.title"
            class="news-card"
          >
            <img
              :src="item.image"
              :alt="item.title"
              class="news-image"
            />

            <div class="news-content">
              <p class="news-date">{{ item.date }}</p>

              <h3>{{ item.title }}</h3>

              <p class="news-description">
                {{ item.description }}
              </p>
            </div>
          </article>
        </div>

      </div>
    </section>

    <!-- PARTNERSHIPS AND MEMBERSHIPS -->
    <section id="partners" class="partners section">
      <div class="container partners-inner">

        <p class="eyebrow">
          CONNECT · COLLABORATE · GROW
        </p>

        <h2>Our Partners <span>& Memberships</span></h2>

        <p class="partners-description">
          Driving technology for education through collaboration
          with academic and industry communities.
        </p>

        <div class="partner-list">
          <div class="partner-item">
            <span>CPU</span>
            <small>Central Philippine University</small>
          </div>

          <div class="partner-item">
            <span>IT</span>
            <small>Technology Community</small>
          </div>

          <div class="partner-item">
            <span>EDU</span>
            <small>Education & Innovation</small>
          </div>
        </div>

      </div>
    </section>

    <!-- FOOTER -->
    <footer id="contact" class="footer">
      <div class="container footer-grid">

        <div class="footer-brand">
          <img
            src="/ccs.png"
            alt="College of Computer Studies Logo"
            class="footer-logo"
          />

          <h3>College of Computer Studies</h3>

          <p>Central Philippine University</p>

          <p>Different people, one goal.</p>
        </div>

        <div class="footer-links">
          <h4>QUICK LINKS</h4>

          <a href="#home">Home</a>
          <a href="#programs">Academic Programs</a>
          <a href="#faculty">Faculty & Staff</a>
          <a href="#news">News & Updates</a>
        </div>

        <div class="footer-contact">
          <h4>CONTACT US</h4>

          <p>Mary Thomas Hall</p>

          <p>Central Philippine University</p>

          <p>Lopez Jaena St., Jaro, Iloilo City</p>

          <a href="mailto:ccssec@cpu.edu.ph">
            ccssec@cpu.edu.ph
          </a>

          <p>Telephone: 329-1971 local 1094</p>
        </div>

      </div>

      <div class="copyright">
        © {{ new Date().getFullYear() }} College of Computer Studies.
        All rights reserved.
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* GENERAL */
.section {
  padding: 90px 24px;
}

.container {
  max-width: 1200px;
  margin: auto;
}

.eyebrow {
  color: #e4bd56;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
}

/* VISION AND MISSION */
.about {
  background: #173d70;
  color: white;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 60px;
}

.about h2 {
  margin: 25px 0;
  color: white;
  font-size: clamp(32px, 4vw, 48px);
  line-height: 1.2;
}

.about h2 span {
  color: #e4bd56;
}

.about-copy {
  color: #e0e7f1;
  font-size: 16px;
  line-height: 1.9;
}

/* NEWS */
.news {
  background: #f5f7fa;
}

.section-heading {
  margin: 0 auto 45px;
  text-align: center;
}

.section-heading .eyebrow {
  color: #b28724;
}

.section-heading h2 {
  color: #173d70;
  font-size: clamp(30px, 4vw, 42px);
}

.section-heading h2 span {
  color: #c19328;
}

.section-heading > p:last-child {
  color: #718096;
  line-height: 1.8;
}

.news-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 25px;
}

.news-card {
  background: white;
  box-shadow: 0 5px 25px #102b4c0a;
  overflow: hidden;
  border-radius: 4px;
}

.news-image {
  display: block;
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.news-content {
  padding: 25px;
}

.news-date {
  color: #b28724;
  font-size: 11px;
  font-weight: 700;
}

.news-content h3 {
  color: #173d70;
  font-size: 18px;
  line-height: 1.5;
}

.news-description {
  color: #718096;
  font-size: 13px;
  line-height: 1.8;
}

/* PARTNERSHIPS */
.partners {
  background: white;
  text-align: center;
}

.partners .eyebrow {
  color: #b28724;
}

.partners h2 {
  color: #173d70;
  font-size: clamp(32px, 4vw, 48px);
  line-height: 1.2;
}

.partners h2 span {
  color: #e4bd56;
}

.partners-description {
  max-width: 650px;
  margin: 0 auto;
  color: #718096;
  line-height: 1.8;
}

.partner-list {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 25px;
  margin: 45px 0 20px;
}

.partner-item {
  display: flex;
  min-height: 130px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 12px;
  background: #f5f7fa;
  border: 1px solid #e8edf3;
}

.partner-item span {
  color: #173d70;
  font-size: 28px;
  font-weight: 900;
}

.partner-item small {
  color: #718096;
}

/* FOOTER */
.footer {
  padding: 65px 24px 0;
  background: #102b4c;
  color: #e4eaf2;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.3fr 0.8fr 1fr;
  gap: 50px;
  padding-bottom: 45px;
}

/* FOOTER IMAGE LOGO */
.footer-logo {
  display: block;
  width: 70px;
  height: 70px;
  object-fit: contain;
  margin-bottom: 15px;
}

.footer h3 {
  color: white;
  font-size: 18px;
}

.footer h4 {
  color: #e4bd56;
  font-size: 12px;
  letter-spacing: 1px;
}

.footer p,
.footer a {
  color: #c5d0df;
  font-size: 13px;
  line-height: 1.9;
}

.footer-links a,
.footer-contact a {
  display: block;
  text-decoration: none;
}

.footer a:hover {
  color: #e4bd56;
}

.copyright {
  padding: 22px 0;
  border-top: 1px solid #ffffff20;
  color: #b7c3d3;
  text-align: center;
  font-size: 12px;
}

/* TABLET */
@media (max-width: 800px) {
  .about-grid,
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 30px;
  }

  .news-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

/* MOBILE */
@media (max-width: 560px) {
  .section {
    padding: 60px 20px;
  }

  .news-grid,
  .partner-list {
    grid-template-columns: 1fr;
  }

  .about-copy {
    font-size: 15px;
  }

  .footer {
    padding-top: 45px;
  }
}
</style>