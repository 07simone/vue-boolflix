<template>
 <nav class="navbar navbar-light bg-dark">
  <div class="container-fluid px-5">
    <h1 class="text">BOOLFIX</h1>
    <div class="d-flex">        <!-- quando premo enter emette un evento che si chiama searchfilm -->
      <input v-model.trim="search" @keyup.enter="$emit('searchFilm',search)" class="form-control me-2" type="search" placeholder="Search" >
      <button  @click="$emit('searchFilm',search)" class="btn btn-outline-success" type="submit">Search</button>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: 'IndexHeader',
  data:function(){
    return{
      search: '', /* variabile per connettere il v-model nell'input*/
              
  }
},

}







</script>


<style scoped lang="scss">
div .navbar-brand{
  
  color:red
}
.text{
    color: red;
  }
img{
    width: 150px;
    height: 100px;
  }
</style>
