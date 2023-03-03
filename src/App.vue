<template>
  <!-- cada componente su propio estado independiente -->
  <!-- el estado global se maneja con vuex -->
  <h1>listado de post import de componentes</h1>
  <PostContainer/>
  <CounterOption/>
  <CounterComposition/> 
  <ExampleSelective/>
  <ExampleFor/>
  <ClassBind/>
  <ModelForm/>
</template>

<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import PostContainer from './components/PostContainer.vue';
import CounterOption from './components/CounterOption.vue';
import CounterComposition from './components/CounterComposition.vue';
import ExampleSelective from './components/ExampleSelective.vue'
import ExampleFor from './components/ExampleFor.vue';
import ClassBind from './components/ClassBind.vue';
import ModelForm from './components/ModelForm.vue';
</script>


<style>
/* aqui se definene estilos generales fuente color etc */
.container{
  border: 1px solid black;
  margin: 10px auto;
  padding: 10px;
}

</style>
