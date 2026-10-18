
<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const programsOpen = ref(false)
const aboutOpen = ref(false)
</script>

<template>
  <header class="site-header">
    <div class="topbar">
      <a href="#home" class="brand">
        <!-- Updated logo image -->
        <img src="/ccs.png" alt="CCS Logo" class="brand-logo" />

        <span class="brand-name">
          COLLEGE OF<br />
          <strong>COMPUTER STUDIES</strong>
          <small>Central Philippine University</small>
        </span>
      </a>

      <button
        class="menu-toggle"
        @click="menuOpen = !menuOpen"
        aria-label="Toggle navigation"
        :aria-expanded="menuOpen"
      >
        ☰
      </button>

      <nav :class="{ 'nav-open': menuOpen }">
        <a href="#home" @click="menuOpen = false">Home</a>

        <div class="nav-dropdown">
          <button @click="aboutOpen = !aboutOpen">
            About Us ▾
          </button>

          <div v-if="aboutOpen" class="dropdown-menu">
            <a href="#history">History</a>
            <a href="#about">Vision & Mission</a>
            <a href="#dean">Message of the Dean</a>
            <a href="#partners">Linkages</a>
          </div>
        </div>

        <div class="nav-dropdown">
          <button @click="programsOpen = !programsOpen">
            Academic Programs ▾
          </button>

          <div v-if="programsOpen" class="dropdown-menu">
            <a href="#programs">Computer Science</a>
            <a href="#programs">Information Technology</a>
            <a href="#programs">Information Systems</a>
            <a href="#programs">
              Digital Media and Interactive Arts
            </a>
            <a href="#programs">Library Information Science</a>
          </div>
        </div>

        <a href="#faculty" @click="menuOpen = false">
          Faculty & Staff
        </a>
        <a href="#news" @click="menuOpen = false">News</a>
        <a href="#contact" @click="menuOpen = false">Contact</a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: #fff;
  box-shadow: 0 2px 12px #00000012;
}

.topbar {
  max-width: 1200px;
  min-height: 88px;
  margin: auto;
  padding: 15px 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 25px;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
  color: #173d70;
  text-decoration: none;
  flex-shrink: 0;
}

.brand-logo {
  display: block;
  width: 54px;
  height: 54px;
  object-fit: contain;
  flex-shrink: 0;
}

.brand-name {
  font-size: 11px;
  line-height: 1.5;
  letter-spacing: 1px;
}

.brand-name strong {
  font-size: 14px;
}

.brand-name small {
  display: block;
  font-size: 9px;
  letter-spacing: 0;
}

nav {
  display: flex;
  align-items: center;
  gap: 18px;
}

nav > a,
.nav-dropdown > button {
  color: #24364c;
  font: inherit;
  font-size: 12px;
  font-weight: 700;
  text-decoration: none;
  background: none;
  border: none;
  cursor: pointer;
}

nav > a:hover,
.nav-dropdown > button:hover {
  color: #c18c19;
}

.nav-dropdown {
  position: relative;
}

.dropdown-menu {
  position: absolute;
  top: 28px;
  left: 0;
  min-width: 220px;
  padding: 8px;
  background: white;
  box-shadow: 0 8px 25px #0002;
  border-radius: 5px;
}

.dropdown-menu a {
  display: block;
  padding: 10px;
  color: #24364c;
  text-decoration: none;
  font-size: 13px;
}

.dropdown-menu a:hover {
  background: #f3f5f8;
}

.menu-toggle {
  display: none;
  border: 0;
  background: transparent;
  font-size: 26px;
  cursor: pointer;
}

@media (max-width: 900px) {
  .menu-toggle {
    display: block;
  }

  nav {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    padding: 20px;
    background: white;
    align-items: stretch;
    flex-direction: column;
    gap: 18px;
  }

  nav.nav-open {
    display: flex;
  }

  .dropdown-menu {
    position: static;
    box-shadow: none;
    border: 1px solid #eee;
    margin-top: 10px;
  }
}
</style>