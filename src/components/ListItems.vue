<template>
   <div  v-for="item in groupedItems" :key="item.id">
    <div class="list-group-item list-group-item-action"> {{item.title}}</div>
   </div>
</template>

<script>
export default {
props: {
    items: {
      type: Array,
      required: true
    }
  },
   computed: {
    groupedItems() {
      if (this.items.length === 0) {
        return
      }
      return this.items
    }
  }
}
</script>

<style>

</style>