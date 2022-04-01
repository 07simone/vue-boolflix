<template>
 <nav class="navbar navbar-light bg-dark">
  <div class="container-fluid px-5">
    <a class="navbar-brand">NETFLIX</a>
    <div class="d-flex">
      <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
      <button class="btn btn-outline-success" type="submit">Search</button>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: 'IndexHeader',
  props: {
    
  }
}
</script>


<style scoped lang="scss">
div .navbar-brand{
  color:red
}
</style>
