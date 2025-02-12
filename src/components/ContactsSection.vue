<template>
<section id="contacts">
  <h1 class="section-title">Elérhetőségek</h1>
  <div class="contacts-wrapper">
    <div class="img-wrapper">
      <img class="map" src="/map.webp" alt="google maps">
    </div>

    <div class="text-wrapper">
      <p class="address">Eger, Széchenyi u. 33.</p>
      <div class="contact">
        <img src="/telephone.webp" alt="phone">
        <div>
          <p>Borosné Müller Tímea</p>
          <p>0620/931-7207</p>
        </div>
      </div>

      <div class="contact">
        <img src="/facebook.webp" alt="facebook">
        <p><a href="https://www.facebook.com/kucko.tanuloszoba">Kuckó Tanulószoba Eger</a></p>
      </div>

      <div class="contact">
        <img src="/mail.webp" alt="email">
        <p>bmtimi@gmail.com</p>
      </div>

      <p>
        A Tanulószoba több belvárosi iskola közelében található,
        így a gyerekek könnyen, akár önállóan is eljuthatnak hozzánk.
        A közelben helyi járatú buszmegálló is található, amely tovább
        egyszerűsíti a megközelítést.
      </p>
    </div>
  </div>
</section>
</template>

<script></script>

<style scoped>
.contacts-wrapper {
  display:          flex;
  align-items:      center;
  justify-content:  center;
  gap:              3.125rem;
}

.contact img { height: 40px; }

.map {
  height:         350px;
  border-radius:  10px;
  box-shadow:     5px 5px 15px 5px hsla(214, 13%, 34%, 0.534);
}

.address {
  font-size:      1.875rem;
  font-weight:    600;
  margin-bottom:  20px;
}

.contact {
  display:        flex;
  align-items:    center;
  gap:            1.25rem;
  margin-bottom:  20px;
}
</style>