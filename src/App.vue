<script setup>
import { ref, computed } from 'vue'

const nome = ref('')
const data = ref('')
const email = ref ('')
const senha = ref ('')
const confirma = ref ('')
const estado = ref('')
const endereco = ref('')
const cidade = ref('')
const hobby = ref('')
const linguagem = ref ([])
const biografia = ref('')
const mostrar = ref (false)


function validar(){
  if( senha.value === confirma.value){
    return true;
  }
  else{
    return false;
  }
}

const mensagem = computed(()=>{
  if(senha.value != confirma.value){
    return 'As senhas são diferentes'
  }
else{
  return ''
}
})
</script>

<template>
  <form @submit.prevent="mostrar = validar()">
    
   
    <label for="text">Nome: </label>
    <input type="text" v-on:keypress="ok= false" v-model="nome" required placeholder="digite seu nome" /> <br>
    
    <br>
    <label for="date">Data de nascimento: </label>
    <input type="date" v-on:keypress="ok= false" v-model="data" required placeholder="data de nascimento" /> <br>
   
<br>
   <label for="text">endereço: </label>
    <input type="text" v-on:keypress="ok=false" v-model="endereco" required placeholder="Digite seu endereço" /><br>
<br>
    <label for="text">cidade: </label>
    <input type="text" v-on:keypress="ok=false" v-model="cidade" required placeholder="Digite sua cidade" /><br>
    
<br>

    <label for="email">Email: </label>
    <input type="email" v-on:keypress="ok= false" v-model="email" required placeholder="digite seu email"/> <br>
   
<br>
<label for="text">Hobby: </label>
    <input type="text" v-on:keypress="ok= false" v-model="hobby" required placeholder="digite seu hobby"/> <br>
    
    <br>
    
    <label for="linguagem">Linguagem de programação: </label>
    <input type="checkbox"  v-model="linguagem" value="python"/>
    <input type="checkbox" v-on:keypress="ok=false" v-model="linguagem" value="PHP"/>
    <input type="checkbox" v-on:keypress="ok=false" v-model="linguagem" value="Javascript"/>
    <br>

    <label for="text">biografia: </label>
    <input type="text" v-on:keypress="ok=false" v-model="biografia" placeholder="Digite sua biografia" /><br>
    <br>




   
  <label for="Estados">Estado</label>
  <select v-on:keypress="ok =false" v-model="estado">
    
    <option value="AC">Acre</option>
    <option value="AL">Alagoas</option>
    <option value="AP">Amapa</option>
    <option value="AM">Amazonas</option>
    <option value="BA">Bahia</option>
    <option value="CE">Ceara</option>
    <option value="DF">Distrito Federal</option>
    <option value="ES">Espirito Santo</option>
    <option value="GO">Goias</option>
    <option value="MA">Maranhão</option>
    <option value="MT">Mato Grosso</option>
    <option value="MS">Mato Grosso do Sul</option>
    <option value="MG">Minas Gerais</option>
    <option value="PA">Pará</option>
    <option value="PB">Paraiba</option>
    <option value="PR">Paraná</option>
    <option value="PE">Pernambuco</option>
    <option value="PI">Piaui</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="RN">Rio Grande do Norte</option>
    <option value="RS">Rio Grande do Sul</option>
    <option value="RO">Rondônia</option>
    <option value="RR">Roraima</option>
    <option value="SC">Santa Catarina</option>
    <option value="SP">São Paulo</option>
    <option value="SE">Sergipe</option>
    <option value="TO">Tocantins</option>
  </select> 
  
  <br><br>

  <label for="password">senha: </label>
    <input type="password" v-on:keypress="ok= false" v-model="senha" required placeholder="digite sua senha"/><br>
    
    <br>
    <label for="password">confirmação de senha: </label>
    <input type="password" v-on:keypress="ok= false" v-model="confirma" required placeholder="digite novamente"/><br>
  
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

