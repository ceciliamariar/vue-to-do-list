<template>
  <section class="w-100 p-4 d-flex justify-content-center pb-4">
   <form class="row g-3 needs-validation" novalidate>
      <div class="col-12">
        <div class="form-outline">
          <label class="form-label">Tarefa</label>
          <input type="text" class="form-control" id="title" v-model="title" />
        </div>
      </div>
      <div class="col-12">
        <button @click="clickAdd" class="btn btn-primary" type="submit">Adicionar</button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
    emits: ['addItem'], 
    methods: {
        clickAdd() {
            this.$emit('addItem', this.title);
        },
    }
    
}
</script>

<style>

</style>