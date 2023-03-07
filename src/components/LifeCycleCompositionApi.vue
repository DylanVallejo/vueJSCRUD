<template>
    <div class="container">
        <h3>Ciclo de vida en Composition API</h3>
        <p>pasado 5 segundos alertara sobre la creacion y montaje de El composition api </p>
    </div>    
</template>
<script setup>
import { onMounted,onUpdated } from 'vue'


//la funcion recibe un callback puede ser un arrow funciton 

    onMounted(()=>{ 
        
        setTimeout(()=>{
            alert('composition api mounted')  
            console.log('composition api mounted')  
            
        },5000)
    })

    onUpdated(()=>{
        setTimeout(()=>{
            
            alert('composition api updated')  
            console.log('composition api updated')  
        },5000)
    })


</script>

<style scoped>

</style>