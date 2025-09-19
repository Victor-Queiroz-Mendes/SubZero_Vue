<template>
  <div class="container">
    <!-- Logo -->
    <div class="logo">logo</div>

    <!-- Título -->
    <h1 class="titulo">Cadastro Do Bar</h1>

    <!-- Formulário -->
    <form @submit.prevent="handleSubmit" class="formulario">
      <p class="descricao">informações sobre o local</p>

      <input v-model="form.nome" type="text" placeholder="Nome do bar" />
      <input v-model="form.email" type="email" placeholder="E-mail" />
      <input v-model="form.cep" type="text" placeholder="CEP" />
      <input v-model="form.tipo" type="text" placeholder="Tipo de bar" />
      <input v-model="form.senha" type="password" placeholder="senha" />

      <button type="submit">Cadastrar</button>
    </form>

    <!-- Rodapé -->
    <footer class="rodape">
      <p>©2025 SeuBarro. Todos os direitos reservados.</p>
      <div class="links">
        <a href="#">Política</a>
        <a href="#">Termos</a>
        <a href="#">FAQ</a>
        <a href="#">Contato</a>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { reactive } from "vue";

const form = reactive({
  nome: "",
  email: "",
  cep: "",
  tipo: "",
  senha: "",
});

const handleSubmit = () => {
  console.log("Dados do formulário:", form);
  alert("Cadastro realizado com sucesso!");
};
</script>

<style scoped>
/* Container geral */
.container {
  min-height: 100vh;
  background: #000;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 10px;
}

/* Logo */
.logo {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  background: #ccc;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #000;
  font-weight: bold;
  margin-bottom: 15px;
  font-size: 16px;
}

/* Título */
.titulo {
  font-size: 22px;
  font-weight: 600;
  margin-bottom: 20px;
}

/* Formulário */
.formulario {
  width: 100%;
  max-width: 320px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.descricao {
  font-size: 13px;
  color: #bbb;
  margin-bottom: 4px;
}

.formulario input {
  padding: 10px 15px;
  border-radius: 25px;
  border: none;
  outline: none;
  font-size: 14px;
  color: #000;
}

.formulario button {
  background: #00bcd4;
  color: #fff;
  padding: 10px;
  border: none;
  border-radius: 25px;
  cursor: pointer;
  font-size: 15px;
  transition: background 0.3s;
}

.formulario button:hover {
  background: #0097a7;
}

/* Rodapé */
.rodape {
  margin-top: 20px;
  width: 100%;
  background: #111;
  color: #aaa;
  font-size: 11px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 6px;
}

.rodape .links {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}

.rodape .links a {
  color: #aaa;
  text-decoration: none;
  transition: 0.3s;
}

.rodape .links a:hover {
  text-decoration: underline;
  color: #fff;
}
</style>
