<template>
  <div class="hello">
    <h1>TextToEncrypt</h1>
    <input v-model="inputText" placeholder="Enter a string" /> <br /><br/>
    <button @click="encrypt()">Encrypt2</button>
    
    <h1>{{resultEncrypt}}</h1> 
  </