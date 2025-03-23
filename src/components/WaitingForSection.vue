<template>
<section>
  <div class="waiting-for-wrapper">
    <h1 class="section-title">{{ waitingfor.title }}</h1>
    <p class="text">{{ waitingfor.firstSection }}</p>
    <p class="text">{{ waitingfor.secondSection }}</p>
    <p class="text" id="who-we-are">{{ waitingfor.thirdSection }}</p>
  </div>
</section>
</template>

<script>
export default {
  props: {
    waitingfor: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.text {
  font-size:  1.125rem;
  margin:     20px 0;
}

@media (max-width: 1024px) {
  .waiting-for-wrapper { margin: 20px; }
}
</style>