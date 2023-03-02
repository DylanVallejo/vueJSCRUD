<template>
    <div class="container">
        <h3>Option api component nos ayudaremos de this para apuntar script no requiere setup aqui no utilizaremos hooks</h3>
        <h3>Valor del contador: {{ counter }} </h3>
        <button @click="addCounter">Incrementar</button>
        <button @click="restCounter" >Restar</button>
        <button @click="resetCounter" >Resetear</button>
        
    </div>
    
    
</template>


<!-- option api no require de ssetup en la etiquerta script  -->
<script>
// nos permite definir que estilo usar 
    import { defineComponent } from 'vue';
    export default defineComponent({
        name: 'CounterOption',
        components: { },
        data(){
            let counter = 0;
            return {counter}
        },
        methods: {
            addCounter() {
                this.counter++
            },
            restCounter(){
                if(this.counter === 0){
                    alert("El contador solo puede llegar hasta 0 ")   
                }else{
                    this.counter--
                    
                }
            },
            resetCounter(){
                this.counter = 0;
            }
        }
    })
    
</script> 

<style scoped>

.container{
    border: 1px solid black;
    margin: 10px auto;
    padding: 10px;
}
</style>