<template>
  <h2>Teste app</h2>
  <edit-item :operation="add"/>
  <list-items :items="this.items"/>
</template>

<script>
import EditItem from './components/EditItem.vue'
import ListItems from './components/ListItems.vue'

export default {
  name: 'App',
  state: {
    items: {}
  },
  components: {
    EditItem, 
    ListItems
  }
}
</script>

<style>

</style>
