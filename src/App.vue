<template>
  <h1 v-bind:class="{ h1App: isSidebar }">Granerateur.</h1>
  <Sidebar v-if="isSidebar" @choice='choice' @menu="menu"></Sidebar>
  <section id="container" v-bind:class="{ containerMenu: isSidebar }">
    <Menu v-if="isMenu" @choice='choice'></Menu>
    <Ville v-if="app === 'ville'"></Ville>
    <Pays v-if="app === 'pays'"></Pays>
    <Prenom v-if="app === 'prenom'"></Prenom>
    <Animaux v-if="app === 'animaux'"></Animaux>
    <Fruit v-if="app === 'fruit'"></Fruit>
    <Nombre v-if="app === 'nombre'"></Nombre>
  </section>
</template>

<script>

import Menu from './components/Menu.vue'
import Ville from './components/Ville.vue'
import Sidebar from './components/Sidebar.vue'
import Pays from './components/Pays.vue'
import Prenom from './components/Prenom.vue'
import Animaux from './components/Animaux.vue'
import Fruit from './components/Fruit.vue'
import Nombre from './components/Nombre.vue'

export default {
  name: 'App',
  components: {
    Menu,
    Ville,
    Sidebar,
    Pays,
    Prenom,
    Animaux,
    Fruit,
    Nombre,
  },
  data() {
      return {
        isMenu: true,
        isSidebar: false,
        app: "",
      }
  },
  methods: {
    choice(payload) {
      console.log(payload)
      this.isMenu = false
      this.isSidebar = true
      this.app = payload
    },

    menu() {
      this.isMenu = true
      this.isSidebar = false
      this.app = ""
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
    min-height: 100%;
  }

  body {
    background-color: #E6EED6;
  }

  h1 {
    font-size: 64px;
    font-family: "Poppins";
  }

  .h1App {
    margin-left: 7%;
  }

  #container {
    display: flex;
    justify-content: center;
    min-height: 80%;
  }

  .containerMenu {
      margin-left: 7%;
  }

  @media screen and (max-width: 1000px) {
        #sidebar{
            display: none;
        }

        .containerMenu {
            margin-left: 0%;
        }

        .h1App {
            margin-left: 0%;
        }
    }

</style>
