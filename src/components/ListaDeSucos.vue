<script setup>
</script>

<template>
    <div>
        <SucoItem nome="Suco De Limão"
            
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
