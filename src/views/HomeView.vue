<template>
  <main class="wrapper">
    <section class="main-section parallax">
      <!-- <div class="background"></div> -->
      <!-- <img src="../assets/tep devanture-car.png" class="background"/> -->
      <h1 class="title">Tout Est Permis</h1>
      <p>Permis Voiture, Moto, Remorque...</p>
    </section>
    <section class="category">
      <h1 class="title">Code de la route</h1>
    </section>
    <section class="code-section parallax">
      <div class="card-container">
        <article :class="showCarCode ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/208.png"/> -->
            <img src="../assets/gpt/code-voiture.png"/>
          </header>
          <footer>
            <h1 @click="showCarCode = !showCarCode">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition>
              <aside v-if="showCarCode">
                <div class="list">
                  <div class="elem"><span>Forfait Code Low Cost</span><span>149€</span></div>
                  <div class="elem"><span>Forfait Code Full</span><span>299€</span></div>
                </div>
              </aside>
            </Transition>
          </footer>
        </article>
        <article :class="showBikeCode ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/208.png"/> -->
            <img src="../assets/gpt/code-moto.png"/>
          </header>
          <footer>
            <h1 @click="showBikeCode = !showBikeCode">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition>
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
      <div class="card-container">
        <article :class="showCar ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/208.png"/> -->
            <img src="../assets/gpt/208-gpt.png"/>
          </header>
          <footer>
            <h1 @click="showCar = !showCar">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition>
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
        <article :class="showBike ? 'large-card card' : 'card'">
          <header>
            <!-- <img src="../assets/bmwrs5.png"/> -->
            <img src="../assets/gpt/moto-bm-gpt-far.png"/>
          </header>
          <footer>
            <h1 @click="showBike = !showBike">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition>
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
        <article :class="showTrailer ? 'large-card card' : 'card'">
          <header>
            <img src="../assets/gpt/remorque-gpt.png"/>
          </header>
          <footer>
            <h1 @click="showTrailer = !showTrailer">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition>
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
        <article :class="showScooter ? 'large-card card' : 'card'">
          <header>
            <img src="../assets/gpt/trott-far-gpt.png"/>
          </header>
          <footer>
            <h1 @click="showScooter = !showScooter">Découvrir nos offres &nbsp;<span class="arrow">&#10095;</span></h1>
            <Transition>
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
    <section>
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Modi eligendi architecto facere odit nemo, magni dicta ipsa officiis maxime nostrum, asperiores doloremque officia quia commodi quidem porro assumenda ea aspernatur in, molestiae aut possimus! Explicabo doloremque delectus quam dolore sit dolorum eligendi totam non atque consequatur corrupti, beatae similique culpa voluptates impedit consectetur blanditiis reiciendis, iste cumque architecto maiores officiis dolorem? Accusantium animi at, quas consequuntur corporis blanditiis aspernatur. Sapiente voluptatem nihil eveniet omnis dolorum dolore! Quibusdam veniam aliquid vero saepe dicta minima iste? Quibusdam ipsam quis quod officia aliquid in ducimus! Iure exercitationem corporis facilis fugit nobis nisi incidunt! Doloribus deserunt quam veritatis fugit sed a assumenda dolores blanditiis iure nostrum cum soluta corporis autem consequuntur, eaque impedit beatae nesciunt. Aliquam consequatur similique tempore quisquam quas nobis dignissimos cum aut dolores impedit a assumenda officia, nihil quibusdam magnam ullam hic sit architecto voluptates animi voluptatibus distinctio! Unde quos, minima explicabo distinctio, quas modi at corrupti, esse ab assumenda incidunt quod sequi tempora accusamus rerum voluptatibus deleniti officia. Ullam quis eius et minus vero itaque deleniti pariatur recusandae veritatis veniam. Ipsa corrupti adipisci laboriosam ad nesciunt explicabo libero ullam a, rem sed ipsam autem nam nulla facilis veniam nobis dolorum repellat. Obcaecati sed tempore omnis dolores voluptas earum maiores iure expedita provident dicta non reiciendis, nemo modi aspernatur recusandae possimus fuga dolorem! A rem dolor provident, laborum aliquam beatae ipsum, quod dolorum eum eos dolorem illo vero quas! Quidem, impedit tempore! Eos corrupti pariatur recusandae voluptatum. Laborum cumque quia provident dignissimos eos temporibus consequuntur sint architecto quas iure optio error, fugiat atque ullam deserunt corrupti at odit officia illum quidem obcaecati quis! Non, saepe nostrum quis atque iusto rerum sit asperiores distinctio sunt temporibus quaerat optio labore illo aut? Nemo eum earum iste et! Ipsam molestias possimus maiores dolorem ullam.
      </p>
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
  }
}
</script>

<style scoped>
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
    background: url('../assets/tep devanture-car-darker-sketch.png');
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
  .category {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: dimgray;
    height: 10vh;
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
  .title {
    width: 100%;
    margin-bottom: 0;
    color: white;
    text-shadow: 0 0 5px black;
    font-size: 8vw;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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
    overflow: auto;
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
    flex: 3 0 25%;
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
  .card header {
    width: 100%;
    aspect-ratio: 16/9;
  }
  .card footer {
    width: 100%;
    min-height: 5vh;
    color: white;
    text-shadow: 0 0 5px black;
    font-size: 1.5vw;
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

  @media only screen and (max-device-width: 1366px) {
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
    .title {
      font-size: 8vh;
    }
    .card header {
      width: 100%;
      aspect-ratio: 16/9;
    }
    .card footer {
      font-size: 1.5vh;
    }
  }
</style>
