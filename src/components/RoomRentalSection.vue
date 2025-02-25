<template>
<section id="roomrental">
  <h1 class="section-title">{{ roomRental.sectionTitle }}</h1>
  <div class="first-row-wrapper">
    <div class="img">
      <img :src="roomRental.image" alt="nagyterem">
    </div>

    <div class="introduction-wrapper">
      <h3 class="int-title">{{ roomRental.title }}</h3>
      <p class="introduction">{{ roomRental.introduction }}</p>

      <div class="rent-wrapper">
        <img class="icon" :src="roomRental.hatUrl" alt="graduation hat">
        <p class="text">{{ roomRental.studyGroup }}</p>
      </div>

      <div class="rent-wrapper">
        <img class="icon" :src="roomRental.bookUrl" alt="book">
        <p class="text">{{ roomRental.workshops }}</p>
      </div>

      <div class="rent-wrapper">
        <img class="icon" :src="roomRental.meetingUrl" alt="meeting">
        <p class="text">{{ roomRental.publicEvents }}</p>
      </div>
    </div>
  </div>

  <div class="second-row-wrapper">
    <div class="equipments-wrapper">
      <h3 class="equip-title">Felszereltség:</h3>
      <div class="equip-row" v-for="x in roomRental.equipments">
        <img class="pipe" src="/checked.webp" alt="pipa">
        <p>{{ x }}</p>
      </div>
    </div>

    <div class="price-wrapper">
      <h3 class="price-title">Foglalás és árak:</h3>
      <div class="equipprice-row" v-for="x in roomRental.prices">
        <p>{{ x }}</p>
      </div>
    </div>
  </div>
</section>
</template>

<script>
export default {
  props: {
    roomRental: Object,
    required: true
  }
}
</script>

<style scoped>
.img img {
  width: 500px;
  border-radius: 10px;
}

.icon { width: 40px }
.pipe { width: 23px; }

.first-row-wrapper {
  display: flex;
  flex-direction: row;
  gap: 30px;
  align-items: center;
}

.rent-wrapper {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
  margin: 10px 0;
}

.introduction {
  margin: 30px 0;
}

.second-row-wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-top: 30px;
}

.equip-row {
  display: flex;
  flex-direction: row;
  margin: 0 0 15px 20px;
}

.equip-title, .price-title { margin-bottom: 10px; }
.equipprice-row {   margin: 0 0 15px 20px; }

.equipments-wrapper,
.price-wrapper { flex: 1; }

@media (max-width: 1024px) {
  #roomrental { margin: 0 20px; }
}

@media (max-width: 768px) {
  .first-row-wrapper,
  .second-row-wrapper {flex-direction: column; }
}

@media (max-width: 425px) {
  .img img { max-width: 300px; }
}
</style>