<script setup>
import { ref } from 'vue';


let message = ref("Hello neegro");
let items = ref(['sai', 'suits', 'gin']);
function add(){
  if(message.value.trim() !== ''){
    items.value.push(message.value.trim());
  }
  message.value = '';
}
</script>

<template>
<button @click="add" >Click me bitch</button>
<input type="text" v-model="message" @keydown.enter="add">
<ul>
  <li v-for="item in items">{{ item }}</li>
</ul>
</template>


