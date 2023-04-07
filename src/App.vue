<template>
  <HelloWorld msg="I am here!"/>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-facing-decorator';
import HelloWorld from './components/HelloWorld.vue';

@Component({
  components: {
    HelloWorld
  }})
export default class App extends Vue 
{

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 160px;
}
</style>
