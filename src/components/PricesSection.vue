<template>
  <div id="prices">
    <img src="/intersecting-wave-layers.webp" alt="Separator" class="separator-img-top">
  </div>
  
  <div class="section">
    <section>
      <h1 class="section-title">Tanszobai árak</h1>
      <div class="prices-wrapper">
        <div class="price-table four-day">
          <div class="price-content">
            <h3 class="price-title">Heti 4 délután</h3>
            <ul>
              <li>
                Rugalmas megoldás azok számára, akik más tevékenységeiket
                is szeretnék összehangolni
              </li>
              <li>
                Négy szabadon választott délután a héten
              </li>
            </ul>
            <p class="price"> 38.000 Ft/hónap</p>
            <p class="discount">Testvérek esetén 3000 Ft/fő kedvezmény</p>
          </div>
        </div>

        <div class="price-table five-day">
          <div class="price-content five">
            <h3 class="price-title">Heti 5 délután</h3>
            <ul>
              <li>
                Ideális azoknak, akik rendszeres támogatást szeretnének
              </li>
              <li>
                Hétfőtől péntekig elérhető programok
              </li>
              <li>
                Folyamatos mentorálás
              </li>
            </ul>
            <p class="price"> 43.000 Ft/hónap</p>
            <p class="discount">Testvérek esetén 3000 Ft/fő kedvezmény</p>
          </div>
        </div>

        <div class="price-table three-day">
          <div class="price-content">
            <h3 class="price-title">Heti 3 délután</h3>
            <ul>
              <li>
                Tökéletes választás a kezdéshez vagy kiegészítő tanuláshoz
              </li>
              <li>
                Három délután, intenzív készségfejlesztéssel
              </li>
              <li>
                Kiemelten fókuszált tanulási program
              </li>
            </ul>
            <p class="price"> 33.000 Ft/hónap</p>
            <p class="discount">Testvérek esetén 3000 Ft/fő kedvezmény</p>
          </div>
        </div>
      </div>

      <div class="prices-description">
          <p>
            Ezek teljes havi díjak, a tanítási szünetek alatt is van
            lehetőség felzárkóztatásra. Amennyiben betegség miatt
            hiányzik a gyermek, adott napokon vagy délelőtt online
            pótolhat.
          </p>
          <p>
            Az első alkalom ingyenes, az első hét próbahét. Ezek után a
            szülőkkel fél éves megállapodást írunk, mivel hosszútávon
            működik jól ez a rendszer.
          </p>
        </div>
    </section>
  </div>
  
  <div id="admission">
    <img src="/intersecting-wave-layers.webp" alt="Separator" class="separator-img-bottom">
  </div>
  </template>

<script></script>

<style scoped>
.section {
  width:            100%;
  background-color: var(--section-bg);
}

section {
  margin:     0 auto;
  padding:    2rem 0;
  text-align: center;
}

.prices-wrapper {
  width:            100%;
  margin-bottom:    50px;
  display:          flex;
  flex-direction:   row;
  flex-wrap:        nowrap;
  justify-content:  space-between;
  align-items:      center;
}

.price-table {
  border-radius:  10px;
  padding:        30px;
  box-shadow:     5px 5px 15px 5px hsla(214, 13%, 34%, 0.534);
  height:         100%;
  display:        flex;
}

.price-content { max-width: 300px; }

.four-day { background-color: var(--prices-orange); }

.five-day {
  background-color: var(--light);
  height:           500px;
  padding:          0 40px;
  display:          flex;
  align-items:      center;
}

.five {
  height:           100%;
  display:          flex;
  flex-direction:   column;
  justify-content:  center;
}

.three-day { background-color: var(--prices-red); }

.price-title {
  border-bottom:  2px solid var(--dark);
  padding-bottom: 10px;
  margin-bottom:  40px;
  font-size:      2.1875rem;
}

ul { list-style: circle inside; }

li { margin-bottom: 20px; }

.price {
  font-family:  "Patrick Hand", serif;
  margin-top:   40px;
  font-size:    2.1875rem;
}

.discount { font-size: 0.875rem; }

.prices-description { text-align: left; }

@media (max-width: 1024px) {
  .prices-wrapper { justify-content: space-around; }
  .price-table { padding: 10px }
  .prices-description { margin: 0 20px; }
}

@media (max-width: 768px) {
  .prices-wrapper {
    flex-direction: column;
  }
  .price-table { margin-bottom: 20px; }
}

@media (max-width: 320px) {
  .price-table { margin: 10px; }
}
</style>