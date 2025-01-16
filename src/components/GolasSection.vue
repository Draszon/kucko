<template>
<section id="goals">
  <div class="goals-wrapper">

    <div class="goal-row">
      <div class="goal-column">
        <div class="goal-container">
          <h1 class="goal-title">Tanulószobánk célja</h1>
          <p class="content">
            Egy barátságos környezet kialakítása a gyerekek számára,
            ahol könnyebb és örömtelibb a tanulás. Nálunk nem csak leckét
            írnak, hanem valódi segítséget kapnak az iskolai tananyag
            megértéséhez és elsajátításához.
          </p>
          <p class="content">
            Kis létszámú csoportjaink lehetővé teszik az egyéni figyelmet,
            így minden gyermek saját tempójában fejlődhet. A házi feladatok
            elkészítésén és a tananyag átismétlésén túl arra próbálunk
            törekedni, hogy magabiztosabbá váljanak, önállóan is tudjanak
            tanulni.
          </p>
        </div>
      </div>
      <div class="goal-column">
        <img src="/irogep.jpg" alt="írógép">
      </div>
    </div>

    <div class="goal-row second-row">
      <div class="goal-column">
        <img src="/tanulas_vagott.jpg" alt="írógép">
      </div>
      <div class="goal-column">
        <div class="goal-container">
          <p class="content">
            Nagy hangsúlyt fektetünk a szociális készségek fejlesztésére is.
            Számos szabadtéri játékkal foglaljuk le őket a tanulás
            végeztével. Programjaink során a gyerekek nem csak tudással,
            hanem új barátságokkal is gazdagodnak. A város különböző
            iskoláiba járnak, itt lehetőség van egymás megismerésére.
          </p>
          <p class="content">
            Ha szeretné, hogy gyermeke olyan közösségben tanuljon, ahol
            figyelem és gondoskodás veszi körül, akkor nálunk a helye.
            Mi azért dolgozunk, hogy minden gyereknek sikerélménye legyen
            és jó jegyek legyenek a bizonyítványban.
          </p>
          <h1 class="goal-title">Mert együtt tényleg könnyebb a tanulás!</h1>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<script></script>

<style scoped>
.goal-row {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.second-row {
  margin-top: 100px;
}

.goal-container {
  width: 70%;
  margin: 0 auto;
}

.goal-title {
  margin: 60px 0;
}

.content {
  font-size: 18px;
  line-height: 2;
  margin: 30px 0;
}

img {
  height: 550px;
  margin: 20px;
}
</style>