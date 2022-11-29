<template >
  <section class="w-100 p-4 d-flex justify-content-center pb-4">
  <div>
    <div  v-for="(item, index) in items" :key="index" class="form-check">
      <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" />
      <label class="form-check-label" for="flexCheckDefault">{{ item.title }}</label>
    </div>
  </div>
  </section>
</template>

<script>
export default {
props: {
    items: Array
  }   
}
</script>

<style>

</style>