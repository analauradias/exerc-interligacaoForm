<script setup>
import { ref } from 'vue';

const nome = ref('');
const idade = ref('');
const email = ref('');

const enviar = ref(true);
const enviar2 = ref(true);

const nome2 = ref('');
const idade2 = ref('');
const email2 = ref('');
</script>

<template>
    <section >
    <div v-if="enviar">
    <input type="text" v-model="nome" placeholder="Digite seu nome">
    <input type="number" v-model="idade" placeholder="Insira sua idade">
    <input type="email" v-model="email" placeholder="Digite seu e-mail">
    <button @click="enviar = false">Enviar</button>
</div>
    <div v-else>
        <h1>Dados:</h1>
        <p>Nome: {{ nome }}</p>
        <p>Idade: {{ idade }}</p>
        <p>E-mail: {{ email }}</p>
        <button @click="enviar = true">Voltar</button>
    </div>
</section>
<section>
    <div v-if="enviar2">
    <input type="text" v-model="nome2" placeholder="Digite seu nome" minlength="3" maxlength="20">
    <input type="number" v-model="idade2" placeholder="Insira sua idade" min="18" max="60">
    <input type="email" v-model="email2" placeholder="Digite seu e-mail">
    <button @click="enviar2 = false">Enviar</button>
    </div>
    <div v-else>
        <h1>Dados:</h1>
        <p>Nome: {{ nome2 }}</p>
        <p>Idade: {{ idade2 }}</p>
        <p>E-mail: {{ email2 }}</p>
        <button @click="enviar2 = true">Voltar</button>
    </div>
</section>
</template>

<style scoped>
   section{
    width: 50%;
   }
</style>


