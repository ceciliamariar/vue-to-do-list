<template>
  <edit-item :operation="add"/>
  <hello-world :msg="Teste"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import EditItem from './components/EditItem.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    EditItem
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
