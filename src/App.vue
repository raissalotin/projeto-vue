<script setup>
import { ref } from 'vue'

const aceitaTermos = ref(false)

</script>

<template>
  <form @submit.prevent="">
  <label for="aceitaTermos">Aceito os termos</label>
  <input type="checkbox" v-model="aceitaTermos" />
  <p>Aceita os termos: </p>
  <label for="sexo">Sexo</label>
  <input type="radio" v-model="sexo" value="masculino" /> Masculino
  <input type="radio" v-model="sexo" value="feminino" /> Feminino
  <p>Sexo: </p>
  <label for="Estados">Estado</label>
  <select v-model="Estados">
    
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
  <p>Estado: </p>
  <button type="submit"></button>
</form>
</template>
