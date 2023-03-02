<template>
    <div class="container">
        <h3>Directiva v-if y v-show</h3>
        <h3 v-show="age < 18">Eres menor de edad tu edad es: {{ age }}</h3>
        <h3 v-show="age >= 18">Eres mayor de edad tu edad es: {{ age }}</h3>
    </div>
</template>

<script setup>
    let age =17;
    // let age2 = 17;
    
    // function esMayor(age){
    //     if(age>18)
        
    // }
    
</script>

<style scoped>
.container{
    border: 1px solid black;
    margin: 10px auto;
    padding: 10px;
}
</style>