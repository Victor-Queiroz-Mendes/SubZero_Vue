<template>
  <button class="btn">
    <slot>Botão</slot>
  </button>
</template>

<script setup>
</script>

<style scoped>
.btn {
  background: #1976d2;
  color: #fff;
  border: none;
  border-radius: 6px;
  padding: 8px 18px;
  font-size: 16px;
  cursor: pointer;
  font-weight: bold;
  transition: background 0.2s;
}
.btn:hover {
  background: #1565c0;
}
</style>
