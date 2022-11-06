<template>
<h2>{{this.operation}}</h2>
 <form>
  <div class="form-group">
    <label for="title">Titulo</label>
    <input type="text" class="form-control" id="title" placeholder="Titulo do item">
  </div>
  <div class="form-group">
    <label for="description">Descrição</label>
    <input type="password" class="form-control" id="description" placeholder="Descrição do item">
  </div>
  <div class="form-group">
    <label for="dateConclusionExpected">Data de conclusão</label>
    <input type="datetime" class="form-control" id="dateConclusionExpected" >
  </div>
  <button type="submit" class="btn btn-primary">{{this.operation}}</button>
</form>
</template>

<script>

import {Item} from '@/models/Item'
import('@/models/Item').Item
export default {

  props: {
    operation: {
      type: String,
      required: true
    },
    item: {
      type: item,
      required: true
    }
  },
  computed: {
    operationTitle() {
      return this.operation == 'add' ? 'Adicionar item' 
              : this.operation == 'edit' ? 'Editar item'
                : '???'
    }
  }
  
}
</script>

<style >

@import'~bootstrap/dist/css/bootstrap.css'

</style>