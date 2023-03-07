<template>
    <div class="container">
        <h4>{{ props.title }}</h4>
        <div class="post">
            <h5></h5>
            <p>{{ props.content }}</p>
        </div>
    </div>
</template>
<script>
import { defineComponent } from 'vue';
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
    setup(props){
        return {props}
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