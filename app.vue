<script setup>
import { ref } from 'vue'

const msg = ref('Compute Product')
const text=ref()
function onInput(number) {
  text.value = number.target.value
} 
const text2=ref()
function onmul(e){
  text2.value=e.target.value
}
const a=ref(true)
const b=ref(false)
 const Compute=ref()
function multiply(){
  Compute.value =text.value*text2.value
     b.value=!b.value

  return a.value=!a.value

  
}
</script>

<template>
  <div class="bg-image" 
     style="background-image: url('https://mdbootstrap.com/img/Photos/Others/images/76.jpg');
            background: cover;
            background-size: cover;
           background-repeat:no-repeat ;
           height: 100vh;
           width:100vw">
      <div class="overlay-text">
        <h1 class="heading"
     style="  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  text-align: center" >
        <h1 >
     {{ msg }}
    </h1>
    <p><input :value="text" @input="onInput" placeholder="Enter first number"><br>
  <input :value="text2" @input="onmul" placeholder="Enter second number">
  <br>
  <button v-if="a" @click="multiply" >
    Compute
    </button>
    <div v-if="b" >
      Product of two numbers is:{{Compute}}
    </div>
  </p>
</h1>
    </div>
	</div>
  
</template>
