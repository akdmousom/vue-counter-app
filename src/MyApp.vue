<script setup>

import {ref} from 'vue'
import HelloWorld from './components/AppHeader.vue';

const count = ref(0)

const countAdd = ()=>{
    if (count.value >= 0) {

        count.value++
        
    }
}

const countMinus = () =>{
    if (count.value !== 0) {

        count.value--
        
    }

  
}


</script>

<template >

    <HelloWorld/>

    <div class="grid justify-center items-center min-h-screen my-auto">
        
        <div>
            <h1 class="text-red-500 text-4xl font-bold text-center">My Vue App</h1>
            <p class="text-red-500 text-3xl my-5 font-bold text-center">Count: {{ count }} </p>
            
            
            <div class="flex justify-center gap-4 my-10">
                
                <button @click="countAdd" class="bg-black hover:first-of-type:text-red-500 hover:first-letter:font-bold  rounded-lg text-white px-2 py-2 text-center">Count +</button>
                <button @click="countMinus" class="bg-black hover:last-of-type:text-red-500 hover:first-letter:font-bold   rounded-lg text-white px-2 py-2 text-center">Count -</button>

             </div>


        </div>

        
        
    </div>

</template>

<style></style>