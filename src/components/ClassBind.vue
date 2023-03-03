<template>
    <div class="container">
        <h3>
            practicando v-bind para clases
        </h3>
        <p :class="{'danger': hasError,}" >Mensaje enviado satisfactoriamente</p>
        <p :class="{'ok': !!hasError,}" >Mensaje enviado satisfactoriamente</p>
        <h3>
            practicando v-bind para estilos
        </h3>
        <p :style="{ backgroundColor: 'purple', color: 'orange' }">Bindeando estilos </p>
        <h3 :style="{backgroundColor: '#ccc', color: color}">
            bind para eventos cambiara de color 
        </h3>
        <button @click="handleClick()">Cambio color</button>
        
    </div>
        
</template>

<script setup>
    import {ref} from 'vue';
    
    let hasError = true;
    let  color = ref('#fff');
    const handleClick = () => {color.value = '#ff0000'}
</script>

<style scoped>
.danger{
    color: red;
}
.ok{
    color: green;
}
</style>
