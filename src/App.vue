<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld />
    
    <p>{{ count }}</p>
    <button v-on:click="increment">Increment</button>
    <button v-on:click="decrement">Decrement</button>
    <ParentComp />
  </div>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++;
    },

    decrement() {
      this.count--;
    }
  }
}
</script>

<style>
#app {
  text-align:center;
  margin-top: 60px;
}

button{
  margin: 5px;
  padding: 10px;
}

</style>
