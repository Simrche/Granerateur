<template>
    <section id="ville">
        <h2>Ville</h2>
        <h3>{{ville}}</h3>
        <Button v-on:click="generateVille()"></Button>
    </section>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "Ville",
    components: {
      Button
    },
    data() {
      return {
        ville: "Appuyez sur le bouton",
        listVille: ["Paris.", "Madrid.", "Londres.", "Rome.", "New York.", "Tokyo.", "Delhi.", "Shanghai.", "Sao Paulo.", "Mexico.", "Le Caire.", "Pekin.", "Istanbul.", "Buenos Aires.", "Rio.", "Bogota.", "Séoul.", "Syndey."]
      }
    },
    methods: {
        generateVille() {
            let number = Math.floor(Math.random() * (this.listVille.length)) + 0;
            this.ville = this.listVille[number]
        }
    }
}
</script>

<style scoped>
    #ville {
        width: 75%;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 100%;
    }

    #ville h2 {
        font-size: 48px;
        font-family: "Poppins";
        font-weight: bold;
    }

    #ville h3 {
        font-size: 72px;
        font-weight: bold;
        font-family: "Poppins";
        margin: 10% 0;
    }
</style>