<template>
  <div class="root">
    <h2 class="title">Hello dear User, you can push the next buttons for a cute popup</h2>
    <div class="container">
      <button class="sellButton" @click="isSellPush = true">Open</button>
      <button class="buyButton" @click="isBuyPush = true" >Buy</button>
    
      <div class="modal" v-if="isSellPush">
       <div>
          <h2>You push the sell button</h2>
          <p>i hope you will sell a good item</p>
          <button @click="isSellPush = false">Close</button>
        </div>
      </div>

      <div class="modal" v-if="isBuyPush">
       <div>
          <h2>You push the buy button</h2>
          <p>i which do you buy a really good item</p>
          <button @click="isBuyPush = false">Close</button>
        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import '~/assets/css/main.css'

const isSellPush = ref(false)
const isBuyPush = ref(false)
</script>

<style>

.root{
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  background: rgb(33, 21, 105);
  padding: 0;
  margin: 0;
  height: 100vh;
  width: 100vw;
  
}

.title{
  align-items: center;
  font-weight: 20px;
  padding-left: 100px;
  color: black;
}

.container{
  padding-top: 100px;
  display: flex;
  align-items: center;
}

.sellButton{
  background: green;
  border-radius: 10px;
  margin: 2px;
  border-style: double;
  text-shadow: 5px;
  box-shadow: grey, 10px;
}

.buyButton{
  
  background: red;
  border-radius: 10px;
  margin: 2px;
  border-style: double;
  text-shadow: 5px;
  box-shadow: grey, 10px;
}
.modal{
  background: black;
  position: absolute;
  align-items: center;
  margin-left: 200px;
  margin-top: 80px;
  padding-left: 200px;
  padding-right: 200px;
  padding-top: 80px;
  padding-bottom: 80px;
  background-color: white;

  
}
</style>