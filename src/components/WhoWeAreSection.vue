<template>
<section id="who-we-are">
<h1 class="section-title">Kik vagyunk?</h1>

<div class="wrapper">
  <div class="img-column">
    <img src="/profilkep.webp" alt="profilkép">
  </div>

  <div class="introduction-column">
    <p class="name">Borosné Müller Tímea, Alapító</p>
    <hr>
    <p class="introduction">Úgy gondolom, fontos, hogy tudd kire bízod a gyermeked, ha a
      Kuckó Tanulószobát választjátok!
    </p>
    <p class="text">Borosné Müller Tímea vagyok, a Kuckó Tanulószoba alapítója.
      Az Eszterházy Károly Tanárképző Főiskolán végeztem
      matematika-számítástechnika tanári szakon 1994-ben, majd a
      Debreceni Egyetem informatika kiegészítőjét végeztem el. 
      Pályafutásomat napközis nevelőként kezdtem, majd informatikát
      és matematikát tanítottam általános- és több középiskolában is.
      Harmadik fiam születése óta a családi vállalkozásunk tagja vagyok,
      de mindig is visszavágytam a tanításhoz.
    </p>
    <p class="text">
      Sajnos a mai közoktatásban
      nem minden gyermek tudja megtanulni, begyakorolnia a tananyagot.
      Ezen szeretnénk segíteni a Tanulószobánkban, ahol a gyerekekkel
      együtt elkészítjük a házi feladatot, az esetleges lemaradásokat
      bepótoljuk. Nem egy tantárgyból korrepetálunk, hanem szinte
      mindenből felkészülünk. Célunk, hogy egyedül is menjen a tanulás,
      több tanulási módszert is alkalmazunk. A folyamatos tanulás a
      jegyeken is meglátszik.
    </p>
    <p class="end">Ha szeretnél gyermekeddel csatlakozni hozzánk, keress bátran!</p>
  </div>
</div>
</section>
</template>

<script></script>

<style scoped>
hr { border: 1px solid var(--dark); }

.wrapper {
  font-size:        1.125rem;
  padding:          80px;
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
</style>