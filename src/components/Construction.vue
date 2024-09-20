<template>
  <main class="main-section">
    <div id="construction">
      <img src="../assets/travaux-en-cours.png" />
      <h1>Ce site est en cours de construction</h1>
      <img src="../assets/travaux-en-cours.png" @click="$emit('clicked')" />
    </div>
  </main>
</template>

<script>
// import store from '@/store'
export default {
  name: 'ContructionBanner'
}
</script>

<style scoped>
#construction {
  display: flex;
  justify-content: center;
  align-items: center;
  /* background-color: rgba(255, 255, 255, 0.8); */
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
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
#construction img {
  width: 15%;
  aspect-ratio: 1;
}
</style>
