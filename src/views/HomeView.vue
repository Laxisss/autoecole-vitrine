<template>
  <main class="wrapper">
    <section class="main-section parallax">
      <!-- <div class="background"></div> -->
      <!-- <img src="../assets/tep devanture-car.png" class="background"/> -->
      <h1 class="main-title">Tout Est Permis</h1>
      <p>Permis Voiture, Moto, Remorque...</p>
    </section>
    <section class="category">
      <h1 class="title">Code de la route</h1>
    </section>
    <section class="code-section parallax">
      <div class="card-container">
        <article ref="carCode" :class="showCarCode ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/208.png"/> -->
            <img src="../assets/gpt/code-voiture.png"/>
            <img src="../assets/back-button.png" @click="scrollTo('bikeCode')" class="scroll-arrow"/>
          </header>
          <footer>
            <h1 @click="showCarCode = !showCarCode">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition name="fadeHeight">
              <aside v-if="showCarCode">
                <div class="list">
                  <div class="elem"><span>Forfait Code Low Cost</span><span>149€</span></div>
                  <div class="elem"><span>Forfait Code Full</span><span>299€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
        <article ref="bikeCode" :class="showBikeCode ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/208.png"/> -->
            <img src="../assets/back-button.png" @click="scrollTo('carCode')" class="scroll-arrow reverse"/>
            <img src="../assets/gpt/code-moto.png"/>
          </header>
          <footer>
            <h1 @click="showBikeCode = !showBikeCode">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition name="fadeHeight">
              <aside v-if="showBikeCode">
                <div class="list">
                  <div class="elem"><span>Forfait Code Low Cost</span><span>149€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
      </div>
    </section>
    <section class="category">
      <h1 class="title">Permis de conduire</h1>
    </section>
    <section class="card-section parallax">
      <div class="card-container" ref="carMenu">
        <article ref="carPermis" :class="showCar ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/208.png"/> -->
            <img src="../assets/gpt/208-gpt.png"/>
            <img src="../assets/back-button.png" @click="scrollTo('bikePermis')" class="scroll-arrow"/>
          </header>
          <footer>
            <h1 @click="showCar = !showCar">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition name="fadeHeight">
              <aside v-if="showCar">
                <div class="list">
                  <div class="elem"><span>Forfait 10h</span><span>509€</span></div>
                  <div class="elem"><span>Forfait 20h</span><span>999€</span></div>
                  <div class="elem"><span>Forfait 20h Traditionnel</span><span>1099€</span></div>
                  <div class="elem"><span>Forfait 20h Accéléré</span><span>1599€</span></div>
                  <div class="elem"><span>Forfait AAC (Conduite Accompagnée)</span><span>1249€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
        <article ref="bikePermis" :class="showBike ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/bmwrs5.png"/> -->
            <img src="../assets/back-button.png" @click="scrollTo('carPermis')" class="scroll-arrow reverse"/>
            <img src="../assets/gpt/moto-bm-gpt-far.png"/>
            <img src="../assets/back-button.png" @click="scrollTo('trailerPermis')" class="scroll-arrow"/>
          </header>
          <footer>
            <h1 @click="showBike = !showBike">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition name="fadeHeight">
              <aside v-if="showBike">
                <div class="list">
                  <div class="elem"><span>Forfait A1 (16 ans)</span><span>999€</span></div>
                  <div class="elem"><span>Forfait A2 (18 ans)</span><span>799€</span></div>
                  <div class="elem"><span>Formation 125cm<sup>3</sup></span><span>279€</span></div>
                  <div class="elem"><span>Permis AM (14 ans)</span><span>349€</span></div>
                  <div class="elem"><span>Passerelle A2 vers A</span><span>279€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
        <article ref="trailerPermis" :class="showTrailer ? 'large-card card' : 'card'">
          <header>
            <img src="../assets/back-button.png" @click="scrollTo('bikePermis')" class="scroll-arrow reverse"/>
            <img src="../assets/gpt/remorque-gpt.png"/>
            <img src="../assets/back-button.png" @click="scrollTo('trottPermis')" class="scroll-arrow"/>
          </header>
          <footer>
            <h1 @click="showTrailer = !showTrailer">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition name="fadeHeight">
              <aside v-if="showTrailer">
                <div class="list">
                  <div class="elem"><span>Forfait A1 (16 ans)</span><span>999€</span></div>
                  <div class="elem"><span>Forfait A2 (18 ans)</span><span>799€</span></div>
                  <div class="elem"><span>Formation 125cm<sup>3</sup></span><span>279€</span></div>
                  <div class="elem"><span>Permis AM (14 ans)</span><span>349€</span></div>
                  <div class="elem"><span>Passerelle A2 vers A</span><span>279€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
        <article ref="trottPermis" :class="showScooter ? 'large-card card' : 'card'">
          <header>
            <img src="../assets/back-button.png" @click="scrollTo('trailerPermis')" class="scroll-arrow reverse"/>
            <img src="../assets/gpt/trott-far-gpt.png"/>
          </header>
          <footer>
            <h1 @click="showScooter = !showScooter">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition name="fadeHeight">
              <aside v-if="showScooter">
                <div class="list">
                  <div class="elem"><span>Formation Trottinette Electrique</span><span>49€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
      </div>
    </section>
    <section class="category">
      <h1 class="title">Nos disponibilités</h1>
    </section>
    <section class="hours-section parallax">
      <div class="row">
        <div class="col">
          <h1 class="title-sm">Horaires du bureau</h1>
          <div class="hour-list">
            <div class="hour-display">
              <span>Lundi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Mardi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Mercredi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Mardi</span><span>Fermé</span>
            </div>
            <div>
              <span>Vendredi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Samedi</span><span>09:30-14:30</span>
            </div>
            <div>
              <span>Dimanche</span><span>Fermé</span>
            </div>
          </div>
        </div>
        <div class="col">
          <h1 class="title-sm">Horaires de conduite</h1>
          <div class="hour-list">
            <div class="hour-display">
              <span>Lundi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Mardi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Mercredi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Mardi</span><span>Fermé</span>
            </div>
            <div>
              <span>Vendredi</span><span>09:30-13:00 | 14:30-19:00</span>
            </div>
            <div>
              <span>Samedi</span><span>09:30-19:00</span>
            </div>
            <div>
              <span>Dimanche</span><span>Fermé</span>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="category">
      <h1 class="title">Nous retrouver</h1>
    </section>
    <section class="location-section parallax">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d181.47118173447035!2d5.399979087845465!3d43.30297692570305!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x12c9bf66a4d12e25%3A0x68515aec28ef4bb9!2sBd%20de%20la%20Blancarde%2C%2013004%20Marseille!5e0!3m2!1sfr!2sfr!4v1702321020452!5m2!1sfr!2sfr" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </section>
    <section class="category legal-tenders">
      <div class="row">
        <div class="col">
          <h6 class="title-xsm">Service Client</h6>
          <p>Batch 1</p>
          <p>Batch 1</p>
          <p>Batch 1</p>
        </div>
        <div class="col">
          <h6 class="title-xsm">Service Client</h6>
          <p>Batch 2</p>
          <p>Batch 2</p>
          <p>Batch 2</p>
        </div>
        <div class="col">
          <h6 class="title-xsm">Nos Services</h6>
          <p>Code de la route</p>
          <p>Permis de conduire</p>
          <p>Rattrapage de points</p>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  watch: {
    showCar (newVal) {
      if(newVal) {
        this.showBike = false
        this.showTrailer = false
        this.showScooter = false
      }
    },
    showBike (newVal) {
      if(newVal) {
        this.showCar = false
        this.showTrailer = false
        this.showScooter = false
      }
    },
    showTrailer (newVal) {
      if(newVal) {
        this.showCar = false
        this.showBike = false
        this.showScooter = false
      }
    },
    showScooter (newVal) {
      if(newVal) {
        this.showCar = false
        this.showTrailer = false
        this.showBike = false
      }
    },
    showCarCode (newVal) {
      if(newVal) {
        this.showBikeCode = false
      }
    },
    showBikeCode (newVal) {
      if(newVal) {
        this.showCarCode = false
      }
    }
  },
  data () {
    return {
      showCar: false,
      showBike: false,
      showTrailer: false,
      showScooter: false,
      showCarCode: false,
      showBikeCode: false
    }
  },
  methods: {
    scrollTo: function (elemToSee) {
      const elem = this.$refs[elemToSee]
      elem.scrollIntoView({
        behavior: 'smooth',
        inline: 'center',
        block: 'center'
      })
    }
  }
}
</script>

<style scoped>
  .card header {
    width: 100%;
    aspect-ratio: 16/9;
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .card footer {
    width: 100%;
    color: white;
    text-shadow: 0 0 5px black;
    font-size: 1.5vw;
  }
  .scroll-arrow {
    visibility: hidden;
    position: absolute;
    /* float: left; */
    /* top: 0; */
    max-width: 40px;
    aspect-ratio: 1!important;
    z-index: 999;
    opacity: 0.7;
  }
  .scroll-arrow:not(.reverse) {
    right: 5px;
  }
  .scroll-arrow.reverse {
    left: 5px;
    transform: rotate(180deg);
  }
  p {
    font-size: 2rem;
  }
  .wrapper {
    height: 100vh;
    width: 100vw;
    overflow-y: auto;
    overflow-x: hidden;
    /* perspective: 10px; */
  }
  .main-section {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    background: url('../assets/Auto_ecole.jpg');
  }
  .main-section p {
    font-size: 2vw;
  }
  .code-section {
    background: url('../assets/route-dessin.png');
    padding: 32px;
    height: fit-content;
  }
  .card-section {
    background: url('../assets/drive.png');
    padding: 32px;
    height: fit-content;
  }
  .hours-section {
    background: url('../assets/timing.png');
    padding: 32px;
    height: fit-content;
  }
  .location-section {
    background: url('../assets/cartoonMap2.png');
    padding: 32px;
    height: fit-content;
  }

  .location-section iframe {
    width: 100%;
    min-height: 30vh;
    box-shadow: 0 0 15px black;
  }
  .category {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: dimgray;
    min-height: 10vh;
    padding: 32px;
  }
  .category .title {
    margin: 0
  }
  .parallax {
    /* Set a specific height */
    /* min-height: 500px; */

    /* Create the parallax scrolling effect */
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  .main-title {
    width: 100%;
    margin-bottom: 0;
    color: white;
    text-shadow: 0 0 5px black;
    font-size: 8vw;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .title {
    width: 100%;
    margin-bottom: 0;
    color: white;
    text-shadow: 0 0 5px black;
    font-size: 5vw;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .title-sm {
    width: 100%;
    color: white;
    text-shadow: 0 0 50px black;
    font-size: 4vw;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .title-xsm {
    width: 100%;
    color: white;
    text-shadow: 0 0 50px black;
    font-size: 2vw;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .col p {
    font-size: 1vw;
    margin-top: 0;
  }
  img {
    width: 100%;
  }
  .arrow {
    transform: rotate(90deg);
    /* Safari */
    -webkit-transform: rotate(90deg);

    /* Firefox */
    -moz-transform: rotate(90deg);

    /* IE */
    -ms-transform: rotate(90deg);

    /* Opera */
    -o-transform: rotate(90deg);
  }
  .card-container {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    flex-wrap: nowrap;
    overflow-x: auto;
    overflow-y: hidden;
    white-space: nowrap;
    min-height: 35vh;
    height: fit-content;
    gap: 1rem;
    width: auto;
  }
  .card {
    flex: 0 0 25%;
    height: 100%;
    border-radius: 16px;
    background-color: rgb(42, 42, 42);
  }
  .large-card {
    flex: 0 0 25%;
  }
  .card:not(.large-card) {
    flex: 0 3 25%;
  }
  .large-card .arrow {
    transform: rotate(-90deg);
    /* Safari */
    -webkit-transform: rotate(-90deg);

    /* Firefox */
    -moz-transform: rotate(-90deg);

    /* IE */
    -ms-transform: rotate(-90deg);

    /* Opera */
    -o-transform: rotate(-90deg);
  }
  .arrow {
    transition: 1s;
  }
  .card footer:hover {
    cursor: pointer;
  }
  .card footer h1 span {
    display: inline-block;
  }
  aside {
    width: calc(100% - 32px);
    transition: height 2s;
    padding: 16px;
  }
  aside .list{
    width: calc(100% - 40px);
    padding: 20px;
  }
  aside .elem {
    text-align: start;
    margin-bottom: 1rem;
    padding-top: 1rem;
    display: flex;
    justify-content: space-between;
    font-size: 1vw;
  }
  .elem + .elem {
    border-top: 1px solid gainsboro;
    padding-top: 1;
  }
  .card img {
    width: 100%;
    object-fit: cover;
    aspect-ratio: 16/9;
    border-top-left-radius: 16px;
    border-top-right-radius: 16px;
  }
  .v-enter-active {
    transition: opacity 1s ease;
  }
  .v-leave-active {
    transition: opacity 0.5s ease;
  }

  .v-enter-from,
  .v-leave-to {
    opacity: 0;
  }

  .fadeHeight-enter-active,
  .fadeHeight-leave-active {
    transition: all 1s;
    max-height: 500px;
  }
  .fadeHeight-enter-from,
  .fadeHeight-leave-to
  {
    opacity: 0;
    max-height: 0px;
  }

  .row {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: row;
    color: white;
    font-weight: bold;
    text-shadow: 0 0 20px black;
    margin-bottom: 0.83em;
    width: 100%;
  }
  .col {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;
    margin-bottom: 1rem;
  }

  .hour-list {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 50%;
    gap: 1rem;
  }
  .hour-list div {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    border-bottom: 1px solid white;
  }

  @media only screen and (max-device-width: 1366px) {
    .scroll-arrow {
      visibility: visible;
    }
    .hour-list {
      width: 90%;
      font-size: 2vw;
    }
    .card {
      /* flex-basis: 90vw!important; */
      flex: 0 0 90vw!important;
      border-radius: 16px;
      background-color: rgb(42, 42, 42);
    }
    .parallax {
      background-attachment: scroll;
    }
    aside .list{
      width: calc(100% - 20px);
      padding: 10px;
      font-size: 2vw;
    }
    aside .elem{
      font-size: 2vw;
    }
    .large-card {
      flex: unset;
    }
    .card:not(.large-card) {
      flex: unset;
    }
    .card-container {
      width: auto;
      justify-content: unset;
    }
    .card-section {
      padding: 16px;
      height: fit-content;
      overflow-x: auto;
    }
    .code-section {
      padding: 16px;
      height: fit-content;
      overflow-x: auto;
    }
    .main-title {
      font-size: 6vh;
    }
    .title {
      font-size: 3vh;
    }
    .card header {
      width: 100%;
      aspect-ratio: 16/9;
    }
    .card footer {
      font-size: 1.5vh;
    }
    .col p {
      font-size: 2vw;
      margin-top: 0;
    }
    .title-xsm {
      width: 100%;
      color: white;
      text-shadow: 0 0 50px black;
      font-size: 4vw;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
  }
</style>
