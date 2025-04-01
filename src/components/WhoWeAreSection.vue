<template>
<section>
<h1 class="section-title">{{ whoWeAre.title }}</h1>

<div class="wrapper">
  <div class="img-column">
    <img src="/profilkep.webp" alt="profilkép">
  </div>

  <div class="introduction-column">
    <p class="name">{{ whoWeAre.name }}</p>
    <hr>
    <p class="introduction">{{ whoWeAre.introduction }}</p>
    <p class="text">{{ whoWeAre.firstSection }}</p>
    <p class="text">{{ whoWeAre.secondSection }}</p>
    <p class="end">{{ whoWeAre.thirdSection }}</p>
  </div>
</div>
</section>
</template>

<script>
export default {
  props: {
    whoWeAre: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
hr { border: 1px solid var(--dark); }

.wrapper {
  font-size:        1.125rem;
  padding:          80px;
  margin:           10px;
  border-radius:    10px;
  background-color: var(--section-bg);
  display:          flex;
  flex-direction:   row;
}

.introduction-column { margin-left: 50px; }

.name {
  font-weight:  600;
  font-size:    1.25rem;
}

.introduction {
  font-style:   italic;
  font-weight:  600;
  margin:       20px 0;
}

.text { margin: 20px 0; }

.end { font-weight: 600; }

.img-column img {
  width:          150px;
  border-radius:  0.625rem;
}

@media (max-width: 768px) {
  .introduction-column { margin-left: 20px; }
  .wrapper { flex-direction: column; padding: 40px 20px;}
  .img-column { text-align: center;  margin-bottom: 30px;}
}

@media (max-width: 425px) {
  .introduction-column { margin: 0; }
}
</style>