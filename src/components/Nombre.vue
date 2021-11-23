<template>
    <section id="nombre">
        <h2>Nombre</h2>
        <h4>MAX : <input type="number" v-model="numberMax"></h4>
        <h3>{{nombre}}</h3>
        <Button v-on:click="generateNombre()"></Button>
    </section>
</template>

<script>
import Button from './Button.vue'

export default {
    name: "Nombre",
    components: {
      Button
    },
    data() {
      return {
        numberMax: 0,
        nombre: "Appuyez sur le bouton",
      }
    },
    methods: {
        generateNombre() {
            let number = Math.floor(Math.random() * (this.numberMax)) + 1;
            this.nombre = number + "."
        }
    }
}
</script>

<style scoped>
    #nombre {
        width: 75%;
        background-color: #BBC5AA;
        border-radius: 60px;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 70vh;
    }

    #nombre h2 {
        font-size: 40px;
        font-family: "Poppins";
        font-weight: bold;
    }

    #nombre h3 {
        font-size: 56px;
        font-weight: bold;
        font-family: "Poppins";
        margin: 10% 0;
    }

    #nombre h4 {
        font-size: 32px;
        margin: 0!important;
        display: flex;
        align-items: center;
        font-weight: bold;
    }

    #nombre h4 input {
        margin-left: 10px;
        height: 32px;
        width: 100px;
        border: none;
        background-color: #E6EED6;
        font-size: 32px;
        text-align: center;
        border-radius: 30px;
        font-weight: bold;
        font-family: "Poppins";
    }

    /* Firefox */
    input[type=number] {
        -moz-appearance: textfield;
    }
    
    /* Chrome */
    input::-webkit-inner-spin-button,
    input::-webkit-outer-spin-button { 
        -webkit-appearance: none;
        margin:0;
    }
    
    /* Opéra*/
    input::-o-inner-spin-button,
    input::-o-outer-spin-button { 
        -o-appearance: none;
        margin:0
    }
</style>