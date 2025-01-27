<template>
<div class="index" id="hero">
  <div class="blur-layer">
    <div class="index-wrapper">
      <div class="index-container">
        <img src="/kucko-logo-jo.webp" alt="kuckó logó" class="index-logo">
        <h1 class="title">Tanulás könnyedén, együtt!</h1>
        <div class="slogans-wrapper">
          <div class="slogan">
            <img src="/sticker3.webp" alt="matek">
            <h1 class="slogan-title">Tanulás</h1>
          </div>
          <div class="slogan">
            <img src="/sticker1.webp" alt="rajzolós">
            <h1 class="slogan-title">Játék</h1>
          </div>
          <div class="slogan">
            <img src="/sticker2.webp" alt="siker">
            <h1 class="slogan-title">Siker</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
</script>

<style scoped>
.index {
  position:   relative;
  max-width:  100%;
  width:      100vw;
  height:     100vh;
  color:      var(--light);
}

.blur-layer {
  position:         relative;
  height:           100%;
  width:            100%;
  background-image: url("/index_hatter.webp");
  background-size:  cover;
}

.index-wrapper {
  height:           100%;
  width:            100%;
  position:         absolute;
  backdrop-filter:  blur(5px);
  background-color: hsla(216, 18%, 16%, 30%);
}

.index-container {
  max-width:        1200px;
  height:           100%;
  margin:           20px auto;
  display:          flex;
  flex-direction:   column;
  align-items:      center;
  justify-content:  center;
}

.index-logo { width: 350px; }

.title { margin: 50px 20px; }

.slogans-wrapper {
  width:            100%;
  display:          flex;
  flex-wrap:        wrap;
  justify-content: space-evenly;
}

.slogan img { width: 190px; }

.slogan-title { text-align: center; }
</style>