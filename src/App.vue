<template>
  <section class="w-100 p-4 d-flex justify-content-center pb-4">
    <h2 class="mb-4">Teste app</h2>
  </section>

  <add-item @addItem="addItem"/>
  <list-items :items="this.items"/>

</template>

<script>
import AddItem from './components/AddItem.vue';
import ListItems from './components/ListItems.vue'

export default {
  name: 'App',
   data() {
        return {
            items: [  ]
        }
    },
    methods: {
        addItem(item) {
          this.items.push( { title: item, completed: false } );
        },
    },
  components: {
    ListItems,
    AddItem
  }
}
</script>

<style>

</style>
