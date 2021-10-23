<template>
    <div id="sidebar">
        <h2>Gra</h2>
        <img src="../assets/drapeau.png" alt="Générateur de Pays" title="Pays">
        <img src="../assets/nombre-de-blocs-jouets.png" alt="Générateur de Nombre" title="Nombre">
        <img src="../assets/nom.png" alt="Générateur de Prénom" title="Prénom">
        <img src="../assets/chien.png" alt="Générateur d'animaux" title="Animaux">
        <img src="../assets/ville.png" alt="Générateur de ville" title="Ville">
        <img src="../assets/fruit.png" alt="Générateur de fruit et légumes" title="Fruit et Légumes">
    </div>
</template>

<script>
export default {
    name: "Sidebar",
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

    #sidebar img:nth-child(7) {
        margin-bottom: 75px
    }

</style>