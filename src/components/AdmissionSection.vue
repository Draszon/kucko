<template>
  <section>
    <h1 class="section-title">{{ admission.sectionTitle }}</h1>
    <div class="admission-wrapper">
      <div class="text-wrapper">
        <h3>{{ admission.introduction }}</h3>
        <p class="introduction">{{ admission.secondIntroduction }}</p>
        <p class="text">{{ admission.firstP }}</p>
        <p class="text">{{ admission.secondP }}</p>
        <p class="prices">{{ admission.prices }}</p>
      </div>

      <div class="img-wrapper">
        <img :src="admission.img" alt="img">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    admission: Object,
    required: true
  }
}
</script>

<style scoped>
.admission-wrapper {
  display:          flex;
  flex-direction:   row;
  align-items:      center;
  justify-content:  space-around;
  flex-wrap:        nowrap;
}

.text-wrapper { width: 600px; }

img {
  width:          350px;
  border-radius:  10px;
}

p, h3{ margin-bottom: 30px; }

.prices { font-weight: 600; }

.introduction {
  font-family:  "Patrick Hand", serif;
  font-size:    1.25rem;
}

@media (max-width: 1024px) {
  .admission-wrapper { margin: 0 20px }
}

@media (max-width: 768px) {
  .admission-wrapper { flex-wrap: wrap; }
  .img-wrapper img { width: 280px; margin: 0; }
}
</style>