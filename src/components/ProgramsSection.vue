<script setup>
const programs = [
  {
    number: '01',
    title: 'Computer Science',
    acronym: 'BSCS',
    icon: '⌘',
    description:
      'Explore algorithms, programming, software development, and the foundations of computing.',
  },
  {
    number: '02',
    title: 'Information Technology',
    acronym: 'BSIT',
    icon: '</>',
    description:
      'Develop skills in IT infrastructure, networks, databases, and modern computing solutions.',
  },
  {
    number: '03',
    title: 'Information Systems',
    acronym: 'BSIS',
    icon: '▤',
    description:
      'Connect business processes with technology, information management, and systems analysis.',
  },
  {
    number: '04',
    title: 'Digital Media and Interactive Arts',
    acronym: 'BSDMIA',
    icon: '✳',
    description:
      'Combine creativity, design, digital media, animation, and interactive technologies.',
  },
  {
    number: '05',
    title: 'Library Information Science',
    acronym: 'BLIS',
    icon: '▥',
    description:
      'Learn about information organization, library services, and information resources.',
  }
]
</script>

<template>
  <section id="programs" class="programs section">
    <div class="container">
      <div class="section-heading">
        <p class="eyebrow">YOUR FUTURE STARTS HERE</p>
        <h2>Explore Our <span>Academic Programs</span></h2>
        <p>
          Build practical skills and prepare for a changing digital world.
        </p>
      </div>

      <div class="program-grid">
        <article
          v-for="program in programs"
          :key="program.number"
          class="program-card"
        >
          <div class="card-top">
            <span class="program-icon">{{ program.icon }}</span>
            <span class="program-number">{{ program.number }}</span>
          </div>

          <span class="acronym">{{ program.acronym }}</span>
          <h3>{{ program.title }}</h3>
          <p>{{ program.description }}</p>

          <a :href="program.link" target="_blank" rel="noopener noreferrer">
            EXPLORE PROGRAM <span>→</span>
          </a>
        </article>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section {
  padding: 95px 24px;
}

.container {
  max-width: 1200px;
  margin: auto;
}

.programs {
  background: #f6f8fb;
}

.section-heading {
  max-width: 700px;
  margin: 0 auto 48px;
  text-align: center;
}

.eyebrow {
  color: #b28724;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
}

.section-heading h2 {
  margin: 15px 0;
  color: #183b69;
  font-size: clamp(30px, 4vw, 44px);
  line-height: 1.2;
}

.section-heading h2 span {
  color: #c19328;
}

.section-heading > p:last-child {
  color: #68758a;
  line-height: 1.8;
}

.program-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 24px;
}

.program-card {
  padding: 30px;
  background: white;
  border: 1px solid #e8edf3;
  transition: transform 0.25s, box-shadow 0.25s;
}

.program-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px #16365b12;
}

.card-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.program-icon {
  display: grid;
  place-items: center;
  width: 54px;
  height: 54px;
  color: #173d70;
  background: #edf2f8;
  font-size: 25px;
  font-weight: 800;
}

.program-number {
  color: #d0d8e2;
  font-size: 27px;
  font-weight: 900;
}

.acronym {
  display: inline-block;
  margin-top: 28px;
  color: #b28724;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 2px;
}

.program-card h3 {
  color: #193a65;
  font-size: 20px;
  line-height: 1.4;
}

.program-card p {
  min-height: 85px;
  color: #697689;
  font-size: 14px;
  line-height: 1.8;
}

.program-card a {
  display: inline-block;
  margin-top: 12px;
  color: #173d70;
  font-size: 11px;
  font-weight: 900;
  letter-spacing: 0.6px;
  text-decoration: none;
}

.program-card a span {
  color: #c19328;
  margin-left: 5px;
}

@media (max-width: 850px) {
  .program-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 560px) {
  .section {
    padding: 65px 18px;
  }

  .program-grid {
    grid-template-columns: 1fr;
  }
}
</style>