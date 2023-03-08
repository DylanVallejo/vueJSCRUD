<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import PostContainer from './components/PostContainer.vue';
import CounterOption from './components/CounterOption.vue';
import CounterComposition from './components/CounterComposition.vue';
import ExampleSelective from './components/ExampleSelective.vue'
import ExampleFor from './components/ExampleFor.vue';
import ClassBind from './components/ClassBind.vue';
import ModelForm from './components/ModelForm.vue';
import LifeCycleOption from './components/LifeCycleOption.vue';
import LifeCycleCompositionApi from './components/LifeCycleCompositionApi.vue';
import PostList from './components/PostList.vue';
import ComputedExample from './components/ComputedExample.vue';
</script>

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
  <LifeCycleOption/>
  <LifeCycleCompositionApi/>
  <PostList/>
  <ComputedExample/>
</template>



<style>
/* aqui se definene estilos generales fuente color etc */
.container{
  border: 1px solid black;
  margin: 10px auto;
  padding: 10px;
  box-sizing: content-box;
}

</style>
