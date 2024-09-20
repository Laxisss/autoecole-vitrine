<template>
  <!-- <header class="nav-header">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
  </header> -->
  <router-view v-if="production"/>
  <Construction v-else/>
</template>

<script>
import Construction from './components/Construction.vue'
export default {
  name: 'AppView',
  components: {
    Construction
  },
  data () {
    return {
      production: false
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.nav-header {
  position: absolute;
  width: 100%;
  top: 5px;
}

nav {
  position: sticky;
  top: 0;
  z-index: 10;
  /* padding: 30px; */
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
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

.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.3s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
</style>
