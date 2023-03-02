<template>
    <div class="container">
        <h3>directiva v-for recorrido de estrucutras</h3>
        <ul>
            <li v-for="person in countries" :key="person.name">{{ person.name }}</li>
        </ul>
    </div>
</template>
<script setup>
    import {ref} from 'vue';
    let countries = ref([
        {name: "dylan" , age: 10},
        {name: "joel",age:12},
        {name: "TryHarder", age:19},
    ])
</script>
<style scoped>

</style>