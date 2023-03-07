<template>
    <div class="container">
        <h3>Creacion de post mediante el uso de la comunicaicon vertical descendente props</h3>
        <div class="container2">
            <PostDetail v-for="elm in info" :key="elm.title" :title="elm.title" :content= "elm.content" />
        </div>
    </div>
</template>

<script setup>
import PostDetail from './PostDetail.vue';
let info = [
    { title: "Post 1", content: "texto de ejemplo 1"},
    { title: "Post 2", content: "texto de ejemplo 2"},
    { title: "Post 3", content: "texto de ejemplo 3"},
    { title: "Post 4", content: "texto de ejemplo 4"},
    { title: "Post 5", content: "texto de ejemplo 5"},
    ]
</script>

<style scoped>
.container .container2{
    display: flex;
    justify-content: wrap;
    flex-direction: row;
    justify-content: space-around;
    box-sizing: border-box ;
}
</style>