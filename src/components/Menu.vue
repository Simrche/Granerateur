<template>
    <section id="menu">
        <div class="buttonApp" v-on:click="choiceApp('pays')">
            <img src="../assets/drapeau.png" alt="Générateur de Pays">
            <div class="buttonAppBot">
                <h2>Générateur de Pays</h2>
            </div>
        </div>
        <div class="buttonApp" v-on:click="choiceApp('nombre')">
            <img src="../assets/nombre-de-blocs-jouets.png" alt="Générateur de Nombre">
            <div class="buttonAppBot">
                <h2>Générateur de Nombre</h2>
            </div>
        </div>
        <div class="buttonApp" v-on:click="choiceApp('prenom')">
            <img src="../assets/nom.png" alt="Générateur de Prénom">
            <div class="buttonAppBot">
                <h2>Générateur de Prénom</h2>
            </div>
        </div>
        <div class="buttonApp" v-on:click="choiceApp('animaux')">
            <img src="../assets/chien.png" alt="Générateur d'animaux">
            <div class="buttonAppBot">
                <h2>Générateur d'Animaux</h2>
            </div>
        </div>
        <div class="buttonApp" v-on:click="choiceApp('ville')">
            <img src="../assets/ville.png" alt="Générateur de ville">
            <div class="buttonAppBot">
                <h2>Générateur de Ville</h2>
            </div>
        </div>
        <div class="buttonApp" v-on:click="choiceApp('fruit')">
            <img src="../assets/fruit.png" alt="Générateur de fruit et légumes">
            <div class="buttonAppBot">
                <h2>Générateur de Fruit & Légumes</h2>
            </div>
        </div>
    </section>
    
</template>

<script>
export default {
    name: "menu",
    data() {
      return {
        
      }
    },
    methods: {
        choiceApp(choice) {
            this.$emit("choice", choice)
        }
    }
}
</script>

<style scoped>

    #menu {
        display: flex;
        width: 75%;
        justify-content: space-around;
        flex-wrap: wrap;
    }

    .buttonApp {
        height: 315px;
        width: 315px;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        cursor: pointer;
        margin: 25px;
        color: #BBC5AA;
    }

    .buttonApp:hover {
        background-color: #c8cfbb;
        transition: 0.3s;
        color: #c8cfbb;
    }

    .buttonApp h2 {
        font-size: 32px;
        font-family: "Poppins";
    }

    .buttonApp img{
        width: 100px;
        margin-top: 50px;
    }

    .buttonAppBot {
        background-color: #090C02;
        height: 120px;
        width: 315px;
        border-bottom-left-radius: 60px;
        border-bottom-right-radius: 60px;
        display: flex;
        align-items: center;
    }
</style>