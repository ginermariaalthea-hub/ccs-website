<template>
  <section id="home" class="hero">
    <div class="hero-overlay">
      <div class="hero-content">
        <p class="eyebrow">
          REMEMBER · CONNECT · ENGAGE · BUILD · SHARE
        </p>

        <h1>
          Different People,<br />
          <span>One Goal.</span>
        </h1>

        <p class="hero-description">
          Discover your potential and shape your future through
          technology, creativity, and innovation.
        </p>

        <a href="#programs" class="hero-button">
          YOUR FUTURE BEGINS HERE →
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 444px;
  background-image:
    linear-gradient(
      90deg,
      rgba(20, 39, 65, 0.92) 0%,
      rgba(35, 52, 75, 0.72) 48%,
      rgba(35, 52, 75, 0.15) 100%
    ),
    url('/campus.png');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

.hero-overlay {
  min-height: 444px;
  display: flex;
  align-items: center;
  background: transparent;
}

.hero-content {
  width: 100%;
  max-width: 1200px;
  padding: 40px 24px;
  margin: auto;
  color: white;
  box-sizing: border-box;
}

.eyebrow {
  margin: 0;
  color: #f8bd42;
  font-size: 12px;
  font-weight: 800;
  letter-spacing: 3px;
  line-height: 1.8;
}

.hero h1 {
  margin: 20px 0 22px;
  font-size: clamp(42px, 6vw, 76px);
  font-weight: 800;
  line-height: 1.08;
  letter-spacing: -2px;
}

.hero h1 span {
  color: #f7c956;
}

.hero-description {
  max-width: 490px;
  margin: 0;
  font-size: 17px;
  line-height: 1.8;
  color: #f1f3f7;
}

.hero-button {
  display: inline-block;
  margin-top: 38px;
  padding: 16px 25px;
  background: #d9a92e;
  color: #17304f;
  font-size: 12px;
  font-weight: 900;
  letter-spacing: 1px;
  text-decoration: none;
  transition: background 0.2s, transform 0.2s;
}

.hero-button:hover {
  background: #f7c956;
  transform: translateY(-2px);
}

@media (max-width: 600px) {
  .hero,
  .hero-overlay {
    min-height: 490px;
  }

  .hero-content {
    padding: 40px 24px;
  }

  .eyebrow {
    font-size: 10px;
    letter-spacing: 1.5px;
  }

  .hero h1 {
    letter-spacing: -1px;
  }

  .hero-description {
    font-size: 16px;
  }
}
</style>