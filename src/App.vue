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
        <h3 class="logo-text" v-if="data">{{ data.name }}</h3>
      </div>

      <nav>
        <ul class="menu-list" v-if="data">
          <li><a href="#hero">{{ data.menu.home }}</a></li>
          <li><a href="#goals">{{ data.menu.goals }}</a></li>
          <li><a href="#waiting-for">{{ data.menu.waiting }}</a></li>
          <li><a href="#who-we-are">{{ data.menu.whoWeAre }}</a></li>
          <li><a href="#prices">{{ data.menu.prices }}</a></li>
          <li><a href="#admission">{{ data.menu.admission }}</a></li>
          <li><a href="#roomrental">{{ data.menu.roomRental }}</a></li>
          <li><a href="#contacts">{{ data.menu.contacts }}</a></li>
        </ul>
      </nav>
    </div>

    <div class="mobile-menu-btn">
      <img @click="navi()" :class="{ 'mobile-menu-open': mobileMenuOpen }" src="/menu-open.svg" alt="menü nyitó gomb">
      <img @click="navi()" src="/menu-close.svg" alt="menü záró gomb">
    </div>
  </header>

  <Transition>
    <div class="mobile-nav" :class="{ 'mobile-open': mobileMenuOpen, 'mobile-close': !mobileMenuOpen }">
      <div class="mobile-wrapper">
        <ul class="mobile-menu-list" v-if="data">
          <li><a @click="navi" href="#hero">{{ data.menu.home }}</a></li>
          <li><a @click="navi" href="#goals">{{ data.menu.goals }}</a></li>
          <li><a @click="navi" href="#waiting-for">{{ data.menu.waiting }}</a></li>
          <li><a @click="navi" href="#who-we-are">{{ data.menu.whoWeAre }}</a></li>
          <li><a @click="navi" href="#prices">{{ data.menu.prices }}</a></li>
          <li><a @click="navi" href="#admission">{{ data.menu.admission }}</a></li>
          <li><a @click="navi" href="#roomrental">{{ data.menu.roomRental }}</a></li>
          <li><a @click="navi" href="#contacts">{{ data.menu.contacts }}</a></li>
        </ul>
      </div>
    </div>
  </Transition>

  <main v-if="data">
    <HeroSection :hero="data?.hero" />
    <GoalsSection :goals="data?.goals" />
    <AmbitionSection :ambitions="data?.ambitions" />
    <WaitingForSection :waitingfor="data?.waitingfor" />
    <WhoWeAreSection :whoWeAre="data?.whoWeAre" />
    <GalerySection :galery="data?.galery" />
    <TheySaidSection :theySaid="data?.theySaid" />
    <PricesSection :prices="data?.prices" />
    <AdmissionSection :admission="data?.admission" />
    <RoomRentalSection :roomRental="data?.roomRental" />
    <ContactsSession :contacts="data?.contacts" />
  </main>

  <footer>
    <div>
      <img src="/intersecting-wave-layers.webp" alt="Separator" class="separator-img-top">
    </div>
    <div class="footer-wrapper" v-if="data">
      <p>Copyright © <span>{{ date }}</span> {{ data.footer.copyright }} | Powered by <a href="http://www.draszon.com">Peter</a></p>
      <p><a href="#">ÁSZF</a> <a href="#">Adatvédelmi nyilatkozat</a></p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      mobileMenuOpen: false,
      date: new Date().getFullYear(),
      data: null
    }
  },
  methods: {
    navi() {
      this.mobileMenuOpen = !this.mobileMenuOpen;
    },
    async fetchData() {
      try {
        const response = await fetch('/content.json');
        this.data = await response.json();
      } catch (error) {
        console.log("Hiba a tartalom betöltése közben!", error);
      }
    }
  },
  async mounted() {
    await this.fetchData();
  }
}
</script>

<style scoped>
/* MOBILE MENU */
.mobile-nav {
  z-index:            1;
  background-color:   hsla(0, 0%, 93%, 68%);
  backdrop-filter:    blur(10px);
  position:           fixed;
  top:                80px;
  right:              0;
  width:              0;
  border-radius:      0 0 0 10px;
  transition:         all .3s;
}

.mobile-menu-list li {
  padding:        20px 40px;
  cursor:         pointer;
  text-transform: uppercase;
  font-family:    "Patrick Hand", serif;
  font-size:      1.125rem;
  border-bottom:  1px solid hsla(0, 0%, 27%, 0.199);
}

.mobile-menu-btn { display: none; }

.mobile-menu-btn img {
  position:   fixed;
  height:     40px;
  right:      20px;
  top:        20px;
}

.mobile-menu-open { display: none; }
.mobile-menu-close { display: block; }

.mobile-open { width: 300px !important; }
.mobile-close { width: 0 !important; }

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

@media (max-width: 1024px) {
  nav { display: none; }
  .mobile-menu-btn { display: block; }
}

@media (max-width: 425px) {
  footer p { text-align: center; }
}
</style>
