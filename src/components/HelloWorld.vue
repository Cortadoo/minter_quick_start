<template>
  <div class="hello">
    <h1>TextToEncrypt</h1>
    <input v-model="inputText" placeholder="Enter a string" /> <br /><br/>
    <button @click="encrypt()">Encrypt2</button>
    
    <h1>{{resultEncrypt}}</h1> 
  </div>
</template>

<script>

export default {  name: "aes-page",
  data: () => ({
     inputText:"",
     resultEncrypt: "",
    }),


    methods: {
        encrypt(){
        
          let key = this.$CryptoJS.enc.Utf8.parse('TRIMULFT1V09O17L1019E2991V09MAPI');
          let iv = this.$CryptoJS.enc.Utf8.parse('2022E2991V09O17L');

          let srcs = this.$CryptoJS.enc.Utf8.parse(this.inputText)
          var encrypted = this.$CryptoJS.AES.encrypt(srcs, key, 
            {
              iv: iv,
         