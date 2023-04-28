<script setup>
import { ref } from 'vue'

const nome = ref('')
const data = ref('')
const email = ref ('')
const senha = ref ('')
const confirma = ref ('')
const estado = ref('')
const endereco = ref('')
const cidade = ref('')
const hobby = ref('')
const linguagem = ref ('')
const biografia = ref('')
const mostrar = ref (false)



</script>

<template>
  <form @submit.prevent="">
    
   
    <label for="text">Nome: </label>
    <input type="text" v-on:keypress="ok= false" v-model="nome" required placeholder="digite seu nome" /> <br>
    <p>o nome digitado é: {{ nome }}</p>
    <br>
    <label for="date">Data de nascimento: </label>
    <input type="date" v-on:keypress="ok= false" v-model="data" required placeholder="data de nascimento" /> <br>
    <p>A data é : {{ data }}</p>
<br>
   <label for="text">endereço: </label>
    <input type="text" v-on:keypress="ok=false" v-model="endereco" required placeholder="Digite seu endereço" />
    <p>O endereço digitado é: {{ endereco }}</p>
  
<br>
    <label for="text">cidade: </label>
    <input type="text" v-on:keypress="ok=false" v-model="cidade" required placeholder="Digite sua cidade" />
    <p>A cidade digitada é: {{ cidade }}</p>
<br>

    <label for="email">Email: </label>
    <input type="email" v-on:keypress="ok= false" v-model="email" required placeholder="digite seu email"/> <br>
    <p>o email digitado é: {{ email }}</p>
<br>
<label for="text">Hobby: </label>
    <input type="text" v-on:keypress="ok= false" v-model="hobby" required placeholder="digite seu hobby"/> <br>
    <p>o hobby digitado é: {{ hobby}}</p>
    <br>
    
    <label for="text">Linguagem de programação: </label>
    <input type="text" v-on:keypress="ok=false" v-model="linguagem" required placeholder="Digite sua linguagem" />
    <p>A linguagem digitada é: {{ linguagem }}</p>
    <br>

    <label for="text">biografia: </label>
    <input type="text" v-on:keypress="ok=false" v-model="biografia" placeholder="Digite sua biografia" />
    <p>A biografia digitada é: {{ biografia }}</p>
    <br>




   
  <label for="Estados">Estado</label>
  <select v-on:keypress="ok =false" v-model="estado">
    
    <option value="12">AC - Acre</option>
    <option value="27">AL - Alagoas</option>
    <option value="16">AP - Amapa</option>
    <option value="13">AM - Amazonas</option>
    <option value="29">BA - Bahia</option>
    <option value="23">CE - Ceara</option>
    <option value="53">DF - Distrito Federal</option>
    <option value="32">ES - Espirito Santo</option>
    <option value="52">GO - Goias</option>
    <option value="21">MA- Maranhão</option>
    <option value="51">MT - Mato Grosso</option>
    <option value="50">MS - Mato Grosso do Sul</option>
    <option value="31">MG - Minas Gerais</option>
    <option value="15">PA - Pará</option>
    <option value="25">PB - Paraiba</option>
    <option value="41">PR - Paraná</option>
    <option value="26">PE - Pernambuco</option>
    <option value="22">PI - Piaui</option>
    <option value="33">RJ - Rio de Janeiro</option>
    <option value="24">RN - Rio Grande do Norte</option>
    <option value="43">RS - Rio Grande do Sul</option>
    <option value="11">RO - Rondônia</option>
    <option value="14">RR - Roraima</option>
    <option value="42">SC - Santa Catarina</option>
    <option value="35">SP - São Paulo</option>
    <option value="28">SE - Sergipe</option>
    <option value="17">TO - Tocantins</option>
  </select> 
  <p>O estado escolhido é é: {{ estado }}</p>
  <br>

  <label for="password">senha: </label>
    <input type="password" v-on:keypress="ok= false" v-model="senha" required placeholder="digite sua senha"/><br>
    <p>a senha digitada é: {{ senha }} </p>
    <br>
    <label for="password">confirmação de senha: </label>
    <input type="password" v-on:keypress="ok= false" v-model="confirma" required placeholder="digite novamente"/><br>
    <p>a confirmação digitada é: {{ confirma}}</p>
    <br>
    
    <button @click="mostrar = !mostrar"> confirmar</button>
  
</form>

<div v-if="mostrar">
<p>o nome digitado é: {{ nome }}</p>
<br>
<p>o endereço é: {{ endereco}}</p>
<br>
<p>a cidade digitada é: {{ cidade}}</p>
<br>
<p>o email digitado é: {{ email}}</p>
<br>
<p>o hobby digitado é: {{ hobby }}</p>
<br>
<p>a linguagem de programação é: {{ linguagem}}</p>
<br>
<p>a biografia digitada é: {{ biografia}}</p>
<br>
<p>o estado escolhido é: {{estado}}</p>
<br>
<p>a senha digitada é: {{ senha }}</p>
<br>
<p>a confirmação digitada é:{{ confirma}}</p>
<br>

</div>

</template>
