<template>
    <button>Générer</button>
</template>

<script>
export default {
    name: 'button'
}
</script>

<style scoped>
    button {
        width: 215px;
        height: 75px;
        border-radius: 35px;
        border: none;
        background-color: #090C02;
        color: #BBC5AA;
        font-size: 32px;
        font-family: "Poppins";
        margin-block-start: 1em;
        margin-block-end: 1em;
        cursor: pointer;
    }

    button:hover {
        background-color: #1c2506;
    }
</style>