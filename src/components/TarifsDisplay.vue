<template>
  <div @mouseover="hover = true" @mouseleave="hover = false">
    <span v-html="libelle"></span>
    <span>{{ prix }}€ 
      <Transition name="slide-fade">
        <span v-if="hover">+></span>
      </Transition>
    </span>
  </div>
</template>

<script>
// import store from '@/store'
export default {
  name: 'TarifsDisplay',
  props: {
    libelle: String,
    prix: Number
  },
  data () {
    return {
      hover: false
      // dataStore: store
    }
  },
  methods: {
    // methods here
  },
  mounted () {
    // mounted here
  },
  created () {
    // created here
  }
}
</script>

<style scoped>
/* Style here */
</style>
