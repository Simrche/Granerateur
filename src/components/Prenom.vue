<template>
    <section id="prenom">
        <h2>Prenom</h2>
        <h3>{{prenom}}</h3>
        <Button v-on:click="generatePrenom()"></Button>
    </section>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "Prenom",
    components: {
      Button
    },
    data() {
      return {
        prenom: "Appuyez sur le bouton",
        listPrenom: ["Simon", "Lili", "Leo", "Arthur", "Margaux", "Cameron", "Alex", "Hugo", "Gabriel", "Rayan", "Owen", "Mael", "Thomas", "Louis", "Julia", "Eva", "Cecile", "Marie", "Astrid", "Matthieu", "Martin"]
      }
    },
    methods: {
        generatePrenom() {
            let number = Math.floor(Math.random() * (this.listPrenom.length)) + 0;
            this.prenom = this.listPrenom[number] + "."
        }
    }
}
</script>

<style scoped>
    #prenom {
        width: 75%;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 100%;
    }

    #prenom h2 {
        font-size: 48px;
        font-family: "Poppins";
        font-weight: bold;
    }

    #prenom h3 {
        font-size: 72px;
        font-weight: bold;
        font-family: "Poppins";
        margin: 10% 0;
    }
</style>