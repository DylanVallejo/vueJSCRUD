<template>
    <div class="container">
        <div class="post">
            <!-- <h5>{{ props.title }}</h5>
            <p>{{ props.content }}</p> -->
            <!-- compositon api -->
            <h5>{{ props.title }}</h5>
            <p>{{ props.content }}</p>
            <input class="input"  type="text" v-model="message"/>
            <button @click="handleClick" >Alert Father </button>
        </div>
    </div>
</template>
<!-- <script >
import { defineComponent,ref } from 'vue';
export default defineComponent({
    name:"PostDetail",
    props: {
        title: {
            type: String,
            required: true
        },
        content : {
            type: String,
            required: true,
            default: "Este post no tiene contenido"
        }
    },
    //emits comunicacion vertical ascendente definimos
    emits: ["alertFather"],
    //props comunicacion vertical descendente desestrucutramos los emits
    setup(props, {emit}){
        let message = ref("")
        const handleClick = () => { 
            console.log(message)
            emit("alertFather", message.value)
        }
        
        return {props, message,handleClick}
    }
    
    // composition api no se usa setup sino data
    // data(props, {emit}){
    //     let message = ref("")
    //     const handleClick = () => { 
    //         console.log(message)
    //         emit("alertFather", message.value)
    //     }
        // debemos usar this en las props y emits 
    //     return {this.props, message,handleClick}
    // }
    
})
</script> -->

<!-- usando composition api para propr y emits -->
<script setup>
    // importamos defineporps y emits para definirlos
    import { ref, defineProps, defineEmits } from 'vue';

    const props = defineProps({title :String, content: String});
    const emit = defineEmits(['alertFather']);
    let message = ref("")
    const handleClick = () => { 
        console.log(message)
        emit("alertFather", message.value)
    }

</script>
<style scoped>
.container .post{
    width: auto;
    height:  150px;
    border-radius: 10px;
    background-color: bisque;
    margin: 10px;
    padding: 10px;
    box-sizing: content-box;
}
.container h4{
    text-align: center;
}
.container .input{
    width: 100px;
    display: block;
}
.container button{
    max-width: auto;
    margin: 2px 0;
    display: block;
}
</style>