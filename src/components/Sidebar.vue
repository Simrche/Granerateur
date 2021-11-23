<template>
    <div id="sidebar">
        <img src="../assets/home.png" alt="Menu" title="Menu" v-on:click="menu()">
        <img src="../assets/drapeau.png" alt="Générateur de Pays" title="Pays" v-on:click="choiceApp('pays')">
        <img src="../assets/nombre-de-blocs-jouets.png" alt="Générateur de Nombre" title="Nombre" v-on:click="choiceApp('nombre')">
        <img src="../assets/nom.png" alt="Générateur de Prénom" title="Prénom" v-on:click="choiceApp('prenom')">
        <img src="../assets/chien.png" alt="Générateur d'animaux" title="Animaux" v-on:click="choiceApp('animaux')">
        <img src="../assets/ville.png" alt="Générateur de ville" title="Ville" v-on:click="choiceApp('ville')">
        <img src="../assets/fruit.png" alt="Générateur de fruit et légumes" title="Fruit et Légumes" v-on:click="choiceApp('fruit')">
    </div>
</template>

<script>
export default {
    name: "Sidebar",
    methods: {
        choiceApp(choice) {
            this.$emit("choice", choice)
        },
        menu() {
            this.$emit("menu")
        }
    }
}
</script>

<style scoped>

    #sidebar {
        position: absolute;
        top: 0;
        left: 0;
        background-color: #BBC5AA;
        height: 100vh;
        width: 7%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
    }

    #sidebar img{
        width: 75px;
        cursor: pointer;
    }

    #sidebar img:first-child {
        width: 50px;
        margin-top: 35px;
        margin-bottom: 35px;
    }

    #sidebar img:nth-child(7) {
        margin-bottom: 75px
    }

    @media screen and (max-width: 1000px) {
        #sidebar{
            display: none;
        }
    }
</style>