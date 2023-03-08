<template>
    <div class="container">
        <h3>Como usar datos computados</h3>
        <div>
            <input type="text" v-model="message" />
            <h4>Mensaje:{{ message }}</h4>
            <h4>Mensaje computado: {{ reverse }}</h4>
        </div>
    </div>
</template>

<script >
import { defineComponent } from 'vue';
export default defineComponent({
    name:'ComputedExample',
    data(){
        return{
            message: ''
        }
    },
    computed : {
        reverse(){
            return this.message.split('').reverse().join(''); 
        }
    }
})
</script>

<style scoped>

</style>