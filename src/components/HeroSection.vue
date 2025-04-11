<template>
<div class="index" id="hero">
  <div class="blur-layer">
    <div class="index-wrapper">
      <div class="index-container">
        <img src="/kucko-logo-jo.webp" alt="kuckó logó" class="index-logo">
        <h1 class="title">{{ hero.title }}</h1>
        <div class="slogans-wrapper">
          <div class="slogan">
            <img src="/sticker3.webp" alt="matek">
            <h1 class="slogan-title">{{ hero.study }}</h1>
          </div>
          <div class="slogan">
            <img src="/sticker1.webp" alt="rajzolós">
            <h1 class="slogan-title">{{ hero.game }}</h1>
          </div>
          <div class="slogan">
            <img src="/sticker2.webp" alt="siker">
            <h1 class="slogan-title">{{ hero.success }}</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  props: {
    hero: {
      type: Object,
      required: true
    }
  }
}
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
  position: relative;
  height: 100vh;
  width: 100%;
  background-image: url("/index_hatter1.jpeg");
  background-size: cover;
  background-position: center center;
  background-attachment: fixed;
  background-repeat: no-repeat;
}


.index-wrapper {
  height:           100%;
  width:            100%;
  position:         absolute;
  backdrop-filter:  blur(10px);
  background-color: hsla(216, 19%, 16%, 0.418);
}

.index-container {
  max-width:        1200px;
  height:           100%;
  margin:           0 auto;
  display:          flex;
  flex-direction:   column;
  align-items:      center;
  justify-content:  center;
}

.index-logo { width: 300px; }

.title {
  margin: 30px 20px;
  font-size: 62px !important;
  text-align: center;
}

.slogans-wrapper {
  width:            100%;
  display:          flex;
  flex-wrap:        wrap;
  justify-content: space-evenly;
}

.slogan {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.slogan img { width: 100px; }

.slogan-title { text-align: center; }

@media (max-width: 768px) {
  .slogan img { width: 80px; }
  .title { font-size: 50px !important; }
}

@media (max-width: 425px) {
  .slogans-wrapper { flex-direction: row; }
  .slogan img { width: 60px; }
  .index-logo { width: 300px; }
  .title { font-size: 40px !important; }
}
</style>