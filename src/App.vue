<template>
  <h1>Granerateur.</h1>
  <section id="container">
    <Menu v-if="isMenu"></Menu>
    <Ville v-if="app === 'ville'"></Ville>
  </section>
</template>

<script>

import Menu from './components/Menu.vue'
import Ville from './components/Ville.vue'

export default {
  name: 'App',
  components: {
    Menu,
    Ville,
  },
  data() {
      return {
        isMenu: true,
        app: "",
      }
  },
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
  min-height: 100%;
}

body {
  background-color: #E6EED6;
}

h1 {
  font-size: 64px;
  font-family: "Poppins";
}

#container {
  display: flex;
  justify-content: center;
  min-height: 80%;
}
</style>
