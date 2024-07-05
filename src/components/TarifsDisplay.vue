<template>
  <div @mouseover="hover = true" @mouseleave="hover = false" class="row-containers" @click="clicked = !clicked">
    <div class="row">
      <span v-html="libelle"></span>
      <span>{{ prix }}€ 
        <Transition name="slide-fade">
          <span v-if="hover && desc">+></span>
        </Transition>
      </span>
    </div>
    <div class="row desc" v-if="clicked" v-html="desc"></div>
  </div>
</template>

<script>
// import store from '@/store'
export default {
  name: 'TarifsDisplay',
  props: {
    libelle: String,
    prix: Number,
    desc: String
  },
  data () {
    return {
      hover: false,
      clicked: false
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
div.row-containers {
  display: flex;
  flex-direction: column;
}
div.row {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.desc {
  color: rgb(158, 158, 158);
  font-size: smaller
}
</style>
