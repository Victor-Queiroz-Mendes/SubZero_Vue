<template>
  <div class="product-card">
    <img :src="image" :alt="nome" class="product-image" />

    <h2 class="product-title">{{ nome }}</h2>
    <p class="product-price">R$ {{ price.toFixed(2) }}</p>

    <button @click="buyProduct" class="buy-btn">Comprar</button>
  </div>
</template>

<script setup>
const props = defineProps({
  nome: {
    type: String,
    required: true
  },
  price: {
    type: Number,
    required: true
  },
  image: {
    type: String,
    required: true
  }
})

const emit = defineEmits(["buy"])

function buyProduct() {
  emit("buy", props.nome)
}
</script>

<style scoped>
.product-card {
  width: 250px;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 12px;
  text-align: center;
  background: #fff;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transition: transform 0.2s;
}

.product-card:hover {
  transform: scale(1.03);
}

.product-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.product-title {
  font-size: 1.2rem;
  margin: 12px 0 6px;
}

.product-price {
  font-size: 1.1rem;
  font-weight: bold;
  color: #2c3e50;
  margin-bottom: 12px;
}

.buy-btn {
  padding: 10px 16px;
  border: none;
  border-radius: 8px;
  background: #3498db;
  color: #fff;
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.2s;
}

.buy-btn:hover {
  background: #2980b9;
}
</style>
