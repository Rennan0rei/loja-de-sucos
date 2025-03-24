<script setup>
</script>

<template>
    <h1> Sucadas Maravilhas</h1>
    <p>Suco de Limão</p>
    <button>Comprar</button>
    <p>Você comprou {{ contador }} vezes</p>
</template>

<script>
export default {
    props: ["nome"],
    data() {
        return { contador: 0};
    },
    methods: {
        comprarSuco() {
            this.contador++;
        },
    },
};
</script>