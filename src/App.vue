<script setup>
import Navbar from './components/Navbar.vue'
import HeroSection from './components/HeroSection.vue'
import ProgramsSection from './components/ProgramsSection.vue'
import FacultySection from './components/FacultySection.vue'
import PartnershipSection from './components/PartnershipSection.vue'
</script>

<template>
  <div class="website">
    <Navbar />

    <main>
      <HeroSection />
      <ProgramsSection />
      <FacultySection />
      <PartnershipSection />
    </main>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap');

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 100px;
}

body {
  margin: 0;
  font-family: 'Inter', Arial, sans-serif;
  color: #24364c;
  background: #fff;
  -webkit-font-smoothing: antialiased;
}

button,
input,
textarea {
  font-family: inherit;
}

img {
  max-width: 100%;
}

a {
  transition: color 0.2s ease;
}

::selection {
  background: #d7a72e;
  color: #102b4c;
}
</style>