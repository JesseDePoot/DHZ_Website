<script setup lang="ts"></script>
<template>
  <div class="hero-bg">
    <video class="video-bg" autoplay muted loop playsinline>
      <source src="/video/hero.mp4" type="video/mp4" />
    </video>
    <div class="hero-content">
      <div class="hero-title">
        <h1>DHZ LEAGUE RACING</h1>
        <h2>Grootste league van Nederland</h2>
      </div>

      <div class="hero-button">
        <a class="btn" href="https://discord.gg/PjqcprSyTE">JOIN DE DISCORD</a>
        <a class="btn">BEKIJK STANDEN</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Wrapper */
.hero-bg {
  position: relative;
  width: 100%;
  min-height: 100vh;
  overflow: hidden;
  isolation: isolate;
}

/* Content */
.hero-content {
  position: absolute;
  display: flex;
  flex-direction: column;

  /* "ongeveer dezelfde plek" op elke schermgrootte */
  top: 50%;
  left: 10%;
  transform: translateY(-50%);

  /* voorkomt dat het te breed wordt op grote schermen */
  max-width: min(800px, 90vw);
}

/* Titels */
.hero-title h1,
.hero-title h2 {
  margin: 0;
}

.hero-title h1 {
  line-height: 1.05;
}

.hero-title h2 {
  margin-top: 0.35rem;
  line-height: 1.2;
}

/* Buttons */
.hero-button {
  display: flex;
  gap: 1rem;
  margin-top: 1.25rem;
  flex-wrap: wrap;
}

/* Achtergrond video */
.video-bg {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: -2;
}

/* Afbeelding + overlay */
.image-wrapper {
  position: relative;
  min-height: 100vh;
}

.image-wrapper img {
  width: 100%;
  height: 100vh;
  display: block;
  object-fit: cover;
}

.overlay {
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.7);
  z-index: 0;
}
</style>
