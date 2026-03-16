<script setup lang="ts"></script>

<template>
  <nav class="nav">
    <div class="nav-side left">
      <a href="#">Competitie</a>
      <a href="#">Kalender</a>
    </div>

    <div class="logo">
      <img src="/images/logo.png" alt="DH2 E-sports logo" />
    </div>

    <div class="nav-side right">
      <a href="#">Geschiedenis</a>
      <a href="#">Over DHZ</a>
    </div>
  </nav>
</template>

<style scoped>
.nav {
  position: fixed;
  top: 24px;
  left: 50%;
  transform: translateX(-50%);

  width: min(1220px, 96%);
  height: 88px;

  background: var(--background);
  border-radius: 32px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  margin: 16px auto 0;
  padding: 0 42px;
  overflow: visible;

  z-index: 9999;
}
.nav-side {
  width: calc(50% - 95px);
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}

.nav a {
  position: relative;
  color: white;
  text-decoration: none;
  text-transform: uppercase;
  font-size: 26px;
  font-weight: 400;
  line-height: 1;
  white-space: nowrap;
  padding: 6px 4px;
}

/* underline hover */
.nav a::after {
  content: "";
  position: absolute;
  left: 50%;
  bottom: -8px;
  width: 100%;
  height: 2px;
  background: white;
  transform: translateX(-50%) scaleX(0);
  transform-origin: center;
  transition: transform 0.25s ease;
}

.nav a:hover::after {
  transform: translateX(-50%) scaleX(1);
}

.logo {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  z-index: 10;

  width: 155px;
  height: 155px;
  border-radius: 50%;
  background: var(--background-light);

  display: flex;
  justify-content: center;
  align-items: center;
}

.logo img {
  width: 128px;
  display: block;
}
</style>
