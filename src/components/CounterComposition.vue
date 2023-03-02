<template>
    <div class="container">
        <h2>Composition Api utilizaremos ref y metodo setup(){} aqui podremos usar hooks y funciones</h2>
        <h3>Valord el contador: {{ counter }}</h3>
        <button @click="addCounter">Incrementar</button>
        <button @click="restCounter" >Restar</button>
        <button @click="resetCounter" >Resetear</button>
    </div>
</template>
<script setup>
// al agreagar setup no dreqquerimos de import y export defineComponents
import { ref } from 'vue';
//podremos escribir codigo directamente
    let counter = ref(0);
    const addCounter = () => {
        counter.value++
    }; 
    
    function restCounter(){
        if(counter.value === 0 ){
            alert('la cnatidad minima es 0 ')
        }else{
            counter.value--
        }
    }
    
    const resetCounter = () => {
        counter.value = 0; 
    };
    // debemos retornas las fucniones y valores sin setup con setup no es necesario
    
</script> 
<style scoped>
.container{
    border: 1px solid black;
    margin: 10px auto;
    padding: 10px;
}
</style>
