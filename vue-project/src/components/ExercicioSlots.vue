<!-- Slot Padrã - Crie um componente ButtonComponent.vue que recebe o texto do botão via slot.  Slots nomeados - Crie um componente com tres slots: header, defoult e footer. -->
 <template>
  <div class="card">
    <div class="card-header">
      <slot name="header">Cabeçalho padrão</slot>
    </div>

    <div class="card-body">
      <slot>Conteúdo padrão</slot>
    </div>

    <div class="card-footer">
      <slot name="footer">Rodapé padrão</slot>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.card {
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 12px;
  max-width: 320px;
  margin: 12px auto;
  background: #f9f9f9;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
.card-header {
  font-weight: bold;
  margin-bottom: 8px;
  font-size: 18px;
}
.card-footer {
  font-size: 14px;
  color: gray;
  margin-top: 8px;
  text-align: right;
}
</style>
<!-- 
<template>
  <div class="app">
    <h1>Exemplo de Slots</h1>

 
    <div class="buttons">
      <ButtonComponent>Salvar</ButtonComponent>
      <ButtonComponent>Cancelar</ButtonComponent>
    </div>


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
import CardComponent from "./components/CardComponent.vue";
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
</style> -->
