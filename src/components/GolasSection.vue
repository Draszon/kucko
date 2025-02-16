<template>
<section id="goals">
  <div class="goals-wrapper">

    <div class="goal-row">
      <div class="goal-column">
        <div class="goal-container">
          <h1 class="goal-title">{{ goals.title }}</h1>
          <p class="content">{{ goals.firstSection }}</p>
          <p class="content">{{ goals.secondSection }}</p>
        </div>
      </div>
      <div class="goal-column">
        <img src="/irogep.webp" alt="írógép">
      </div>
    </div>

    <div class="goal-row second-row">
      <div class="goal-column">
        <img src="/tanulas_vagott.webp" alt="írógép">
      </div>
      <div class="goal-column">
        <div class="goal-container">
          <p class="content">{{ goals.thirdSection }}</p>
          <p class="content">{{ goals.fourthSection }}</p>
          <h1 class="goal-title">{{ goals.goal }}</h1>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<script>
export default {
  props: {
    goals: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.goal-row {
  display:          flex;
  flex-direction:   row;
  justify-content:  center;
  align-items:      center;
}

.second-row { margin-top: 50px; }

.goal-container {
  width:  70%;
  margin: 0 auto;
}

.goal-title { margin: 60px 0; }

.content {
  font-size:    18px;
  line-height:  2;
  margin:       30px 0;
}

img {
  height:         550px;
  margin:         20px;
  border-radius:  10px;
}

@media (max-width: 768px) {
  .goal-row {flex-direction: column; }
  .second-row { flex-direction: column-reverse; }
}

@media (max-width: 425px) {
  .goal-column img { height: 350px; margin: 0; }
  .goal-container { width: 90%; }
}
</style>