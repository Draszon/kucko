<template>
<section id="galery">
  <h1 class="section-title">Nézz be hozzánk</h1>
  <div class="galery-wrapper">

    <div class="left-arrow">
      <img class="arrow left" src="/right-arrow.webp" alt="arrow">
    </div>

    <div class="galery">
      <img src="/galery/kucko3.webp" alt="szoba">
    </div>

    <div class="image-description">
      <h3 class="image-title">Tanulóasztalok</h3>
      <p class="description">
        Tágas és kényelmes asztalok, ahol a gyerekek együtt tanulhatnak,
        házi feladatot készíthetnek és segíthetik egymást a fejlődésben.
      </p>
    </div>

    <div class="right-arrow">
      <img class="arrow right" src="/right-arrow.webp" alt="arrow">
    </div>
  </div>
</section>
</template>

<script></script>

<style scoped>
.galery-wrapper {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.galery-wrapper div { margin: 0px 20px; }

.arrow {
  width:  35px;
  cursor: pointer;
}

.left { transform: scaleX(-1); }

.galery img {
  width:          550px;
  border-radius:  10px;
}
</style>