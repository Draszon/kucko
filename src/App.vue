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
import RoomRentalSection from './components/RoomRentalSection.vue'
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
          <li><a href="#roomrental">terembérlés</a></li>
          <li><a href="#contacts">elérhetőségek</a></li>
        </ul>
      </nav>
    </div>
    <div class="mobile-menu-btn">
      <img @click="navi()" :class="{ 'mobile-menu-close': mobileMenuOpen }" class="menu-open" src="/menu-open.svg" alt="menü nyitó gomb">
      <img @click="navi()" :class="{ 'mobile-menu-open': mobileMenuOpen }" class="menu-close" src="/menu-close.svg" alt="menü záró gomb">
    </div>
  </header>

  <Transition>
    <div class="mobile-nav">
      <div class="mobile-wrapper">
        <ul class="mobile-menu-list">
          <li><a href="#hero">kezdőlap</a></li>
          <li><a href="#goals">céljaink</a></li>
          <li><a href="#waiting-for">kiket várunk</a></li>
          <li><a href="#who-we-are">kik vagyunk</a></li>
          <li><a href="#prices">árak</a></li>
          <li><a href="#admission">felvételi</a></li>
          <li><a href="#roomrental">terembérlés</a></li>
          <li><a href="#contacts">elérhetőségek</a></li>
        </ul>
      </div>
    </div>
  </Transition>

  <main>
    <HeroSection />
    <GoalsSection />
    <AmbitionSection />
    <WaitingForSection />
    <WhoWeAreSection />
    <GalerySection />
    <TheySaidSection />
    <PricesSection />
    <AdmissionSection />
    <RoomRentalSection />
    <ContactsSession />
  </main>

  <footer>
    <div>
      <img src="/intersecting-wave-layers.webp" alt="Separator" class="separator-img-top">
    </div>
    <div class="footer-wrapper">
      <p>Copyright © 2025 Kuckó tanulószoba| Powered by <a href="http://www.draszon.com">Peter</a></p>
      <p><a href="#">ÁSZF</a> <a href="#">Adatvédelmi nyilatkozat</a></p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style scoped>
/* MOBILE MENU */

.mobile-nav {
  z-index:            1;
  background-color:   hsla(0, 0%, 93%, 68%);
  position:           fixed;
  top:                80px;
  right:              0;
  width:              300px;
  border-radius: 0 0 0 10px;
}

.mobile-menu-list li {
  padding:        20px 40px;
  cursor:         pointer;
  text-transform: uppercase;
  font-family:    "Patrick Hand", serif;
  font-size:      1.125rem;
  border-bottom:  1px solid hsla(0, 0%, 27%, 0.199);
}

.mobile-menu-btn {
  display: none;
}

.mobile-menu-btn img {
  position:   fixed;
  height:     40px;
  right:      20px;
  top:        20px;
}

.mobile-menu {
  z-index:            1;
  background-color:   var(--section-light-bg);
  font-weight:        500;
  width:              100%;
  position:           fixed;
  top:                60px;
  display:            flex;
  flex-direction:     column;
  height:             0;
  transition:         .2s;
  overflow:           hidden;
}

/* ----------- */

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
  width:            100%;
  margin:           0 20px;
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

.footer-wrapper {
  background-color: var(--section-bg);
  height:           100px;
  display:          flex;
  flex-direction:   column;
  align-items:      center;
  justify-content:  center;
}

.footer-wrapper p { margin-bottom: 10px; }

footer a { margin: 0 10px; }

/* ---- */
</style>
