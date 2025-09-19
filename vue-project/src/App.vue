<template>
  <div class="app">
    <h1>Exemplo de Slots</h1>

    <!-- Usando slot padrão no botão -->
    <div class="buttons">
      <ButtonComponent>Salvar</ButtonComponent>
      <ButtonComponent>Cancelar</ButtonComponent>
    </div>

    <!-- Usando slots nomeados no card -->
    <CardComponent>
      <template #header>
        <h3>Card com Slots</h3>
      </template>

      <p>Esse é o conteúdo principal do card.</p>

      <template #footer>
        <ButtonComponent>Fechar</ButtonComponent>
      </template>
    </CardComponent>
  </div>
</template>

<script setup>
import ButtonComponent from "./components/ButtonComponent.vue";
import CardComponent from "./components/ExercicioSlots.vue";
</script>

<style scoped>
.app {
  font-family: Arial, sans-serif;
  padding: 20px;
  text-align: center;
}

.buttons {
  margin-bottom: 20px;
  display: flex;
  justify-content: center;
  gap: 10px;
}
</style>
