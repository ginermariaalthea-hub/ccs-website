<script setup>
const faculty = [
  {
    name: 'Ma. Christina A. Quijano, MSCS',
    role: 'Dean',
    image: '/Dean.png'
  },
  {
    name: 'Marjee Rose B. Parreñono, MSCS, MBA',
    role: 'Program coordinator (BSCS, BSDMIA, and MSCS)',
    image: '/pinky.jpg'
  },
  {
    name: 'Rea P. Balontong, MBA',
    role: 'Department Head (IT & IS)',
    image: '/rea.jpg'
  }
]
</script>

<template>
  <div>
    <section id="history" class="history section">
      <div class="container history-grid">
        <div class="history-image">
          <img
            src="/cpucampus.jpg"
            alt="Central Philippine University campus"
          />

          <div class="history-label">
            <strong>1995</strong>
            <span>Where our story began</span>
          </div>
        </div>

        <div class="history-content">
          <p class="eyebrow">REMEMBER · OUR STORY</p>
          <h2>How It <span>Started</span></h2>

          <p>
            The College of Computer Studies began in 1995 with the
            Bachelor of Science in Computer Science program under
            the College of Commerce.
          </p>

          <p>
            From its beginnings, the college has continued to develop
            students through computing education, innovation, and
            opportunities for lifelong learning.
          </p>
        </div>
      </div>
    </section>

    <section id="dean" class="dean section">
      <div class="container dean-grid">
        <div class="dean-content">
          <p class="eyebrow">ENGAGE · LEARN · GROW</p>
          <h2>Message from <span>the Dean</span></h2>

          <blockquote>
            “The primary focus of CCS is teaching and learning.
            We encourage our students to grow through academic
            experiences, friendship, fellowship, and opportunities
            to achieve their dreams.”
          </blockquote>

          <h3>Ma. Christina A. Quijano, MSCS</h3>
          <p class="dean-role">
            Dean, College of Computer Studies
          </p>
        </div>

        <div class="dean-decoration">
          <img
            src="/Dean.png"
            alt="Dean Ma. Christina A. Quijano"
            class="dean-photo"
          />
          <p>Different people. One goal.</p>
        </div>
      </div>
    </section>

    <section id="faculty" class="faculty section">
      <div class="container">
        <div class="section-heading">
          <p class="eyebrow">OUR PEOPLE</p>
          <h2>Meet Our <span>Faculty</span></h2>
          <p>
            Academically knowledgeable and here to support your journey.
          </p>
        </div>

        <div class="faculty-grid">
          <article
            v-for="(person, index) in faculty"
            :key="person.name + index"
            class="faculty-card"
          >
            <img :src="person.image" :alt="person.name" />

            <div class="faculty-info">
              <h3>{{ person.name }}</h3>
              <p>{{ person.role }}</p>
            </div>
          </article>
        </div>

        <div class="center">
          <a href="#faculty" class="outline-button">
            OUR FACULTY & STAFF
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.section {
  padding: 90px 24px;
}

.container {
  max-width: 1200px;
  margin: auto;
}

.history-grid,
.dean-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 70px;
}

/* HISTORY */
.history-image {
  position: relative;
  min-width: 0;
}

.history-image img {
  width: 100%;
  height: 430px;
  display: block;
  object-fit: cover;
  object-position: center;
  border-radius: 2px;
}

.history-label {
  position: absolute;
  right: -20px;
  bottom: 25px;
  padding: 22px 28px;
  background: #173d70;
  color: white;
}

.history-label strong {
  display: block;
  color: #f2c65e;
  font-size: 36px;
}

.history-label span {
  font-size: 12px;
}

/* HEADINGS */
.eyebrow {
  color: #b28724;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
}

.history-content h2,
.dean-content h2,
.section-heading h2 {
  color: #183b69;
  font-size: clamp(30px, 4vw, 43px);
  line-height: 1.2;
}

.history-content h2 span,
.dean-content h2 span,
.section-heading h2 span {
  color: #c19328;
}

.history-content > p:not(.eyebrow) {
  color: #6c7788;
  line-height: 1.9;
  font-size: 15px;
}

/* DEAN */
.dean {
  background: #f4f6f9;
}

.dean-content blockquote {
  margin: 25px 0;
  padding-left: 22px;
  border-left: 4px solid #d2a22f;
  color: #606e80;
  font-size: 16px;
  font-style: italic;
  line-height: 1.9;
}

.dean-content h3 {
  color: #173d70;
  font-size: 17px;
}

.dean-role {
  color: #7c8795;
  font-size: 13px;
}

.dean-decoration {
  min-height: 330px;
  padding: 25px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #173d70;
  color: white;
  box-sizing: border-box;
}

.dean-photo {
  width: 220px;
  height: 240px;
  object-fit: cover;
  object-position: center top;
  border: 4px solid #e4bd56;
}

.dean-decoration p {
  color: #f2c65e;
  font-weight: 700;
  letter-spacing: 1px;
  text-align: center;
}

/* FACULTY */
.faculty {
  background: white;
}

.section-heading {
  max-width: 700px;
  margin: 0 auto 45px;
  text-align: center;
}

.section-heading > p:last-child {
  color: #6c7788;
  line-height: 1.8;
}

.faculty-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 25px;
}

.faculty-card {
  background: #f5f7fa;
  overflow: hidden;
}

.faculty-card img {
  width: 100%;
  height: 300px;
  display: block;
  object-fit: cover;
  object-position: center top;
}

.faculty-info {
  padding: 22px;
  text-align: center;
}

.faculty-info h3 {
  color: #173d70;
  font-size: 16px;
}

.faculty-info p {
  color: #9b7829;
  font-size: 13px;
}

.center {
  margin-top: 40px;
  text-align: center;
}

.outline-button {
  display: inline-block;
  padding: 15px 22px;
  border: 1px solid #173d70;
  color: #173d70;
  font-size: 11px;
  font-weight: 900;
  text-decoration: none;
}

.outline-button:hover {
  background: #173d70;
  color: white;
}

/* RESPONSIVE */
@media (max-width: 750px) {
  .section {
    padding: 60px 20px;
  }

  .history-grid,
  .dean-grid {
    grid-template-columns: 1fr;
    gap: 35px;
  }

  .history-image img {
    height: 320px;
  }

  .history-label {
    right: 0;
  }

  .faculty-grid {
    grid-template-columns: 1fr;
  }

  .faculty-card img {
    height: 340px;
  }

  .dean-decoration {
    min-height: 280px;
  }
}
</style>