<template>
<div>
  <img src="/intersecting-wave-layers.webp" alt="Separator" class="separator-img-top">
</div>

<div class="section">
  <section>
    <h1 class="section-title">Törekvésünk, hogy a gyerekek</h1>
    <div class="ambitions-wrapper">
      <div class="ambition">
        <img src="/studying.webp">
        <p class="ambition-text">Megtanuljanak tanulni</p>
      </div>
      <div class="ambition">
        <img src="/help.webp">
        <p class="ambition-text">Merjenek kérdezni</p>
      </div>
      <div class="ambition">
        <img src="/funy_to_study.webp">
        <p class="ambition-text">Érezzék jól magukat tanulás közben</p>
      </div>
      <div class="ambition">
        <img src="/önbizalom.webp">
        <p class="ambition-text">Ne küzdjenek az önbizalomhiánnyal, ismerjék meg saját értékeiket, képességeiket</p>
      </div>
    </div>
  </section>
</div>

<div id="waiting-for">
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

.ambitions-wrapper {
  display:          flex;
  flex-wrap:        wrap;
  flex-direction:   row;
  justify-content:  center;
  align-items:      center;
}

.ambition {
  width:    300px;
  height: 330px;
  padding:  0 1.875rem;
}

.ambition img {
  height:         200px;
  margin-bottom:  1.875rem;
}

.ambition-text {
  font-size:    1.125rem;
  line-height:  1.3;
}
</style>