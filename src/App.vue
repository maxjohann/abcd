<script setup>
import { ref } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmaSenha = ref('')
const data = ref('')
const endereço = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagemProg = ref('')
const biografia = ref('')
const aceitar = ref(false)
</script>

<template>
    <form class="info" @submit.prevent="enviar()">
      <p>Nome:</p>
      <input type="text" v-model="nome" minlength="3" maxlength="20"/>
      <p>email:</p>
      <input type="email" v-model="email"/>
      <p>senha:</p>
      <input type="password" v-model="senha">
      <p>confirmar senha:</p>
      <input type="password" v-model="confirmaSenha">
      <p>data de nascimento:</p>
      <input type="date" v-model="data">
      <p>endereço:</p>
      <input type="text" v-model="endereço">
      <P>cidade:</P>
      <input type="string" v-model="cidade">
      <p>estado:</p>
      <select type="string" v-model="estado">
        <option>AC</option>
        <option>AL</option>
        <option>AP</option>
        <option>AM</option>
        <option>BA</option>
        <option>CE</option>
        <option>DF</option>
        <option>ES</option>
        <option>GO</option>
        <option>MA</option>
        <option>MT</option>
        <option>MS</option>
        <option>MG</option>
        <option>PA</option>
        <option>PB</option>
        <option>PR</option>
        <option>PE</option>
        <option>PI</option>
        <option>RJ</option>
        <option>RN</option>
        <option>RS</option>
        <option>RO</option>
        <option>RR</option>
        <option>SC</option>
        <option>SP</option>
        <option>SE</option>
        <option>TO</option>
      </select>
      <p>hobbies:</p>
      <input type="text" v-model="hobbies">
      <p>linguagem de Programação:</p>
      <input type="text" v-model="linguagemProg">
      <p>biografia:</p>
      <input type="text" v-model="biografia">
      <hr>
      <button type="submit" @click="aceitar = !aceitar">Enviar</button>
    </form>
  <div v-if="aceitar" id="div">
<p>{{ nome }}</p>
<p>{{ email }}</p>
<p>{{ senha }}</p>
<p>{{ data }}</p>
<p>{{ endereço }}</p>
<p>{{ cidade }}</p>
<p>{{ estado }}</p>
<p>{{ hobbies }}</p>
<p>{{ linguagemProg }}</p>
<p>{{ biografia }}</p>
  </div>
</template>


<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}
h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
#div {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin: 0px 0px 0px 50px;
  height: fit-content;
}
</style>
