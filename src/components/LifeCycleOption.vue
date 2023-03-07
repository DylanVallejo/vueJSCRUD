<template>
    <div class="container">
        <h3>Ciclo de vida en Option API</h3>
        <p>al crear el componente alertara sobre su creacion y montaje </p>
    </div>    
</template>
<script>

    import { defineComponent } from 'vue'

    export default defineComponent({
        name: "LifeCycleOption",
        data(){
            
        },
        methods(){
            
        },
        // usando ciclos de vida 
        //creacion del elemento
        created(){
            alert("option api created ")
        },
        //componente montado
        mounted(){
            alert("option api mounted")
            
        },
        //componente actualizado
        updated(){
            alert("option api updated")
        },
        //destroy
        unmounted(){
            alert("option api unmounted")
        },
    })
    
</script>
<style scoped>

</style>