<template>
    <section id="pays">
        <h2>Pays</h2>
        <h3>{{pays}}</h3>
        <Button v-on:click="generatePays()"></Button>
    </section>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "Pays",
    components: {
      Button
    },
    data() {
      return {
        pays: "Appuyez sur le bouton",
        listPays: ["France", "Espagne", "Angleterre", "Allemagne", "Argentine", "Irlande", "Chine", "Ecosse", "Portugal", "Autriche", "Algérie", "Maroc", "Suisse", "Croatie", "Italie", "Russie", "Japon", "Australie", "Canada", "Mexique", "Bresil", "Inde", "Afrique du Sud"]
      }
    },
    methods: {
        generatePays() {
            let number = Math.floor(Math.random() * (this.listPays.length)) + 0;
            this.pays = this.listPays[number] + "."
        }
    }
}
</script>

<style scoped>
    #pays {
        width: 75%;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 100%;
    }

    #pays h2 {
        font-size: 48px;
        font-family: "Poppins";
        font-weight: bold;
    }

    #pays h3 {
        font-size: 72px;
        font-weight: bold;
        font-family: "Poppins";
        margin: 10% 0;
    }
</style>