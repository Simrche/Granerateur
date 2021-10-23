<template>
    <section id="animaux">
        <h2>Animaux</h2>
        <h3>{{animaux}}</h3>
        <Button v-on:click="generateAnimaux()"></Button>
    </section>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "Animaux",
    components: {
      Button
    },
    data() {
      return {
        animaux: "Appuyez sur le bouton",
        listAnimaux: ["Lion.", "Chat.", "Chien."]
      }
    },
    methods: {
        generateAnimaux() {
            let number = Math.floor(Math.random() * (this.listAnimaux.length)) + 0;
            this.animaux = this.listAnimaux[number]
        }
    }
}
</script>

<style scoped>
    #animaux {
        width: 75%;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 100%;
    }

    #animaux h2 {
        font-size: 48px;
        font-family: "Poppins";
        font-weight: bold;
    }

    #animaux h3 {
        font-size: 72px;
        font-weight: bold;
        font-family: "Poppins";
        margin: 10% 0;
    }
</style>