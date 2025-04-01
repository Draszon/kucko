<template>
<section id="galery">
  <h1 class="section-title">{{ galery.sectionTitle }}</h1>
  <div class="galery-wrapper">

    <div class="left-arrow">
      <img @click="imgCountDown()" class="arrow left" src="/right-arrow.webp" alt="arrow">
    </div>

    <div class="img-desc-wrapper" >
      <Transition name="img" mode="out-in">
        <div :key="imgCounter" class="galery">
          <img :src="galery.imgs[imgCounter].url" alt="szobák">
        </div>
      </Transition>

      <Transition name="text" mode="out-in">
        <div :key="imgCounter" class="image-description">
          <h3 class="image-title">{{ galery.imgs[imgCounter].title }}</h3>
          <p class="description">{{ galery.imgs[imgCounter].description }}</p>
        </div>
      </Transition>
    </div>

    <div class="right-arrow">
      <img @click="imgCountUp()" class="arrow right" src="/right-arrow.webp" alt="arrow">
    </div>
  </div>
</section>
</template>

<script>
export default {
  props: {
    galery: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      imgCounter: 0,
    }
  },
  methods: {
    imgCountUp() {
      if (this.imgCounter > this.galery.imgs.length - 2) {
        this.imgCounter = 0;
      } else {
        this.imgCounter++;
      }
    },
    imgCountDown() {
      if (this.imgCounter <= 0) {
        this.imgCounter = this.galery.imgs.length - 1;
      } else {
        this.imgCounter--;
      }
    }
  }
}
</script>

<style scoped>
.text-enter-active,
.text-leave-active {
  transition: all .5s ease-out;
}

.text-enter-from {
  opacity: 0;
  transform: translateY(100px);
}

.text-enter-to,
.text-leave-to {
  opacity: 1;
  transform: translateY(0);
}

.text-leave-to {
  opacity: 0;
  transform: translateY(-100px);
}

.img-enter-active,
.img-leave-active {
  transition: all .4s ease-out;
}

.img-enter-from {
  opacity: 0;
  transform: scale(0);
}

.img-enter-to,
.img-leave-to {
  opacity: 1;
  transform: scale(1);
}

.img-leave-to {
  opacity: 0;
  transform: scale(0);
}

.galery-wrapper {
  height:           420px;
  display:          flex;
  flex-direction:   row;
  align-items:      center;
  justify-content:  center;
}

.galery-wrapper div { margin: 0px 20px; }

.img-desc-wrapper {
  display:        flex;
  flex-direction: row;
  align-items:    center;
}

.arrow {
  width:  35px;
  cursor: pointer;
}

.left { transform: scaleX(-1); }

.galery img {
  width:          550px;
  border-radius:  10px;
}

@media (max-width: 1024px) {
  .galery img { width: 400px; }
  .img-desc-wrapper { margin: 0 !important; }
}

@media (max-width: 768px) {
  .galery-wrapper { flex-direction: row; }
  .img-desc-wrapper { flex-direction: column; }
  .galery img { width: 300px; }
  .left-arrow, .right-arrow { margin: 0 !important; }
}

@media (max-width: 425px) {
  .galery img { width: 200px; }
  .arrow { width: 20px; }
}
</style>