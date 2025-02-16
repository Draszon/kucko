<template>
  <section>
    <h1 class="section-title">Felvételi felkészítő nyolcadikosoknak</h1>
    <div class="admission-wrapper">
      <div class="text-wrapper">
        <h3>Lépj magabiztosan a középiskolába!</h3>
        <p class="introduction">
          A középiskolai felvételi az egyik legfontosabb mérföldkő a
          diákok életében. Mi azért vagyunk, hogy ezt a kihívást
          magabiztosan és felkészülten vegyék.
        </p>
        <p class="text">
          Október elejétől a januári vizsgáig hetente egy-egy alkalommal
          2x45 percben tartunk foglalkozásokat matematikából és magyar
          nyelvből. Szisztematikusan átismételjük az általános iskolai
          tananyagot, külön kitérve a felvételi feladatsorban
          leggyakrabban előforduló feladattípusokkal. Ilyen többek
          között magyarból a helyesírás, az érvelés és a szövegértés,
          matematikából a szöveges feladatok, a geometria, algebra,
          logikai feladatok.
        </p>
        <p class="text">
          A felkészülés vége felé több próbafelvételit írunk, együtt
          kijavítjuk, megbeszéljük a megoldásokat is. A kemény munka
          meghozza gyümölcsét: a gyerekek magabiztosan vágnak neki az
          első nagy megmérettetésüknek.
        </p>
        <p class="prices">
          Ára: tanszobásoknak 1500 FT/ 90 perc,
          külsősöknek 3000 FT/90 perc.
        </p>
      </div>

      <div class="img-wrapper">
        <img src="/study2.webp" alt="img">
      </div>
    </div>
  </section>
</template>

<script></script>

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

.introduction, .prices { font-weight: 600; }

@media (max-width: 1024px) {
  .admission-wrapper { margin: 0 20px }
}

@media (max-width: 768px) {
  .img-wrapper img { width: 300px; margin-left: 10px; }
}

@media (max-width: 425px) {
  .admission-wrapper { flex-wrap: wrap; }
  .img-wrapper img { width: 280px; margin: 0; }
}
</style>