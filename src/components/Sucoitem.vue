<template>
    <div>
        <h3>{{ nome }}</h3>
        <input 
            placeholder="Quantidade"
            type="number"
            v-model="quantidade"
            min="0"
            step="1"
            @input="validarQuantidade"
        />
        <button @click="comprarSuco">Comprar</button>
        <button @click="removerSuco">Remover</button>
        <p>Comprado {{ sacola }} vezes</p>
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
            if (this.quantidade > 0) {
                this.sacola += this.quantidade;
            }
        },
        removerSuco() {
            if (this.quantidade > 0) {
                this.sacola -= this.quantidade;
                if (this.sacola < 0) {
                    this.sacola = 0;
                }
            }
        },
        validarQuantidade() {
            this.quantidade = Math.max(0, Math.floor(this.quantidade) || 0);
        }
    },
};
</script>
