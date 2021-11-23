<template>
    <section id="fruit">
        <h2>Fruit & Légumes</h2>
        <h3>{{fruit}}</h3>
        <Button v-on:click="generateFruit()"></Button>
    </section>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "Fruit",
    components: {
      Button
    },
    data() {
      return {
        fruit: "Appuyez sur le bouton",
        listFruit: ["Pomme", "Banane", "Poire", "Pêche", "Tomate", "Pomme de terre", "Carotte", "Salade", "Aubergine", "Asperge", "Concombre", "Courgette", "Litchi", "Clémentine", "Mangue", "Fraise", "Poireau", "Poivron", "Brocoli", "Dattes", "Raisin", "Framboise", "Kiwi"]
      }
    },
    methods: {
        generateFruit() {
            let number = Math.floor(Math.random() * (this.listFruit.length)) + 0;
            this.fruit = this.listFruit[number] + "."
        }
    }
}
</script>

<style scoped>
    #fruit {
        width: 75%;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 70vh;
    }

    #fruit h2 {
        font-size: 48px;
        font-family: "Poppins";
        font-weight: bold;
    }

    #fruit h3 {
        font-size: 72px;
        font-weight: bold;
        font-family: "Poppins";
        margin: 10% 0;
    }
</style>