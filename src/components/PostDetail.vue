<template>
    <div class="container">
        <div class="post">
            <h5>{{ props.title }}</h5>
            <p>{{ props.content }}</p>
            <input  type="text" v-model="message"/>
            <button @click="handleClick" >Alert Father Component</button>
        </div>
    </div>
</template>
<script>
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
})
</script>
<style scoped>
.container .post{
    width: 200px;
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
</style>