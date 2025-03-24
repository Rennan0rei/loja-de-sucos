<script setup>
</script>

<template>
    <div>
        <h3>{{ nome }}</h3>
        <input placeholder="Quantidade"
               type="number"
               v-model="quantidade" />
    </div>
</template>

<script>
export default {
    props: ["nome"],
    data() {
        return {
            sacola: 0,
            quantidade: 0,
        };
    },
    methods: {
        comprarSuco() {
            this.sacola = this.quantidade + this.sacola;
            console.log(this.sacola)
        },
    },
};
</script>