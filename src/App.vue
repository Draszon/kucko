<script setup>
import HeroSection from './components/HeroSection.vue'
import GoalsSection from './components/GolasSection.vue'
import AmbitionSection from './components/AmbitionSection.vue'
import WaitingForSection from './components/WaitingForSection.vue'
import PricesSection from './components/PricesSection.vue'
import WhoWeAreSection from './components/WhoWeAreSection.vue'
import ContactsSession from './components/ContactsSection.vue'
import AdmissionSection from './components/AdmissionSection.vue'
import TheySaidSection from './components/TheySaidSection.vue'
import GalerySection from './components/GalerySection.vue'
</script>

<template>
  <header>
    <div class="header-wrapper">
      <div class="logo-wrapper">
        <img class="logo" src="/ures-haz.png" alt="üres ház logó">
        <h3 class="logo-text">kuckó tanulószoba</h3>
      </div>

      <nav>
        <ul class="menu-list">
          <li><a href="#hero">kezdőlap</a></li>
          <li><a href="#goals">céljaink</a></li>
          <li><a href="#waiting-for">kiket várunk</a></li>
          <li><a href="#who-we-are">kik vagyunk</a></li>
          <li><a href="#prices">árak</a></li>
          <li><a href="#admission">felvételi</a></li>
          <li><a href="#contacts">elérhetőségek</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <HeroSection />
    <GoalsSection />
    <AmbitionSection />
    <WaitingForSection />
    <WhoWeAreSection />
    <GalerySection />
    <TheySaidSection />
    <AdmissionSection />
    <PricesSection />
    <ContactsSession />
  </main>
</template>

<style scoped>
/* HEADER */
header {
  z-index:          100;
  width:            100%;
  height:           80px;
  background-color: hsla(0, 0%, 93%, 68%);
  display:          flex;
  align-items:      center;
  position:         fixed;
  backdrop-filter:  blur(10px);
  border-bottom:    1px solid hsl(0, 0%, 80%);
}

.header-wrapper {
  width:            1200px;
  margin:           0 auto;
  display:          flex;
  flex-wrap:        nowrap;
  justify-content:  space-between;
}

.logo-wrapper {
  display:      flex;
  flex-wrap:    nowrap;
  align-items:  center;
}

.logo {height: 60px;}

.logo-text { text-transform: uppercase; }

nav {
  display:      flex;
  align-items:  center;
}

.menu-list {
  display:        flex;
  flex-wrap:      wrap;
  text-transform: uppercase;
  font-family:    "Patrick Hand", serif;
  font-size:      1.125rem;
}

.menu-list li {
  margin:         0.625rem;
  padding:        0.3125rem;
  cursor:         pointer;
  border-bottom:  2px solid hsla(0, 0%, 0%, 0%);
  transition:     border-bottom .2s;
}

.menu-list li:hover {
  border-bottom:  2px solid var(--dark);
  transition:     border-bottom .2s;
}
/* ---- */


/* FOOTER */

/* ---- */
</style>
