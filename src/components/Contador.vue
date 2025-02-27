<script setup lang="ts">
import { ref } from "vue";
import Button from "primevue/button";

const contador = ref(0);

function incrementar() {
    contador.value++;
}
function decrementar() {
    contador.value--;
}
function reset() {
    contador.value = 0;
}
</script>

<template>
    <h1>Contador em: {{ contador }}</h1>
    <hr />
    <Button @click="incrementar">Incrementar</Button>
    <Button @click="decrementar">Decrementar</Button>
    <Button @click="reset" :disabled="contador === 0">Resetar</Button>
</template>

<style scoped></style>
