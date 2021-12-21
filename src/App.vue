<template>
  <div id="app">
    <lifecycle />
    <button @click="toggle">Toggle if</button>
    {{ plusGrand }}
  </div>
</template>

<script>
import Lifecycle from "./components/Lifecycle.vue"

export default {
  name: 'App',
  components: {
    Lifecycle
  },
  data() {
    return {
      visible: true,
      pfff: ':)'
    }
  },
  computed: {
    plusGrand() {
      if (this.pfff === ':)') return ':D'
      else return 'D:'
    }
  },
  methods: {
    toggle() {
      if (this.pfff === ':)') this.pfff = ':('
      else this.pfff = ':)'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
