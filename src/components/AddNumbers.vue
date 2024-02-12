<template>
    <div>
    <br><input type="text" v-model="n1" placeholder="Enter First Number">  &nbsp;
        <input type="text" v-model="n2" placeholder="Enter second Number"> &nbsp;
        <button @click="addNumbers">ADD</button> <br>
        <!-- <input type="text" v-model="n1" placeholder="Enter second Number">  -->
        <!-- <p> Sum : {{  n1}} + {{ n2}}</p> -->
        <h2>Total : <span id="sum">{{ totalsum}}</span></h2>
    </div>
</template>

<script setup>

import { ref } from 'vue';

const n1 = ref('')
const n2 = ref('')
 const totalsum= ref(0)


const addNumbers = () => {
    totalsum.value = Number(n1.value) + Number(n2.value);

}
totalsum.value = ""
</script>
<style>

body{

        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
    
      
}

h2{
    margin-top: 50px;
}
#sum{
    width: 100px;
    height: 50px;
    background-color: rgb(175, 18, 18);
}
</style>