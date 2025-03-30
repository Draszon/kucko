<template>
<section id="contacts">
  <h1 class="section-title">{{ contacts.sectionTitle }}</h1>
  <div class="contacts-wrapper">
    <div class="img-wrapper">
      <a :href="contacts.mapLink" target="_blank"><img class="map" :src="contacts.mapImg" alt="google maps"></a>
    </div>

    <div class="text-wrapper">
      <p class="address">{{ contacts.address }}</p>
      <div class="contact">
        <img :src="contacts.phoneIcon" alt="phone">
        <div>
          <p>{{ contacts.name }}</p>
          <p>{{ contacts.phone }}</p>
        </div>
      </div>

      <div class="contact">
        <img :src="contacts.faceIcon" alt="facebook">
        <p><a target="_blank" :href="contacts.facebookLink">{{ contacts.facebookName }}</a></p>
      </div>

      <div class="contact">
        <img :src="contacts.mailIcon" alt="email">
        <p>{{ contacts.mail }}</p>
      </div>

      <p>{{ contacts.content }}</p>
    </div>
  </div>
</section>
</template>

<script>
export default {
  props: {
    contacts: Object,
    required: true
  }
}
</script>

<style scoped>
.contacts-wrapper {
  display:          flex;
  align-items:      center;
  justify-content:  center;
  gap:              3.125rem;
}

.contact img { height: 40px; }

.map {
  height:         350px;
  border-radius:  10px;
  box-shadow:     5px 5px 15px 5px hsla(214, 13%, 34%, 0.534);
}

.address {
  font-size:      1.875rem;
  font-weight:    600;
  margin-bottom:  20px;
}

.contact {
  display:        flex;
  align-items:    center;
  gap:            1.25rem;
  margin-bottom:  20px;
}

@media (max-width: 1024px) {
  .contacts-wrapper { margin: 0 20px; }
  .img-wrapper img { height: 300px; }
}

@media (max-width: 768px) {
  .contacts-wrapper { flex-wrap: wrap; }
  .text-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .contact { width: 250px; }
}

@media (max-width: 425px) {
  .img-wrapper img { height: 220px; }
}

@media (max-width: 320px) {
  .img-wrapper img { height: 180px; }
}
</style>