<script setup>
const props = defineProps({
    name: String,
    email: String,
    telefone: String,
    idade: Number,
    ativo: Boolean,
})
</script>

<template>
    <div class="card" v-if="props.name">
        <h3>{{ props.name }}</h3>
        <p v-if="props.email">Email: {{ props.email }}</p>
        <p v-if="props.telefone">Telefone: {{ props.telefone }}</p>
        <p v-if="props.idade">Idade: {{ props.idade }}</p>
        <div :class="props.ativo ? 'ativo' : 'inativo'">
            Status: {{ props.ativo ? 'Ativo' : 'Inativo' }}
        </div>
    </div>
</template>
<style scoped> 
    .card {
        border: 1px solid #ccc;
        border-radius: 8px;
        padding: 1rem;
        margin: 1rem;
        box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1);
    }
    .ativo {
        color: green;
    }
    .inativo {
        color: red;
    }
</style>
