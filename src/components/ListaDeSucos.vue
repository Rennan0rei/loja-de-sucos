<script setup>
</script>

<template>
    <div>
        <SucoItem
            v-for="suco in sucos"
            :key="suco"
            :nome="suco"
        />
    </div>
</template>

<script>
import SucoItem from './Sucoitem.vue';

export default {
    components: { SucoItem },
    data() {
        return { sucos: ["Laranja", "Maçã", "Uva"] };
    },
};
</script>
