<template>
<h2>{{operationTitle()}}</h2>
<h2>Teste</h2>
 <form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-group form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="submit" class="btn btn-primary">{{operationTitle()}}</button>
</form>
 <hello-world msg="Adicione um novo item" />
</template>

<script>
export default {
  components: {
    HelloWorld    
  },
  props: {
    operation: {
      type: String,
      required: true
    }
  },
  computed: {
    operationTitle() {
      return this.operation == 'add' ? 'Adicionar item' 
              : this.operation == 'edit' ? 'Editar item'
                : 'add'
    },
  }
}
</script>

<style >
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

@import'~bootstrap/dist/css/bootstrap.css'

</style>