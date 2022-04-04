<template>
  <div class="card p-3">
        
      <div class="card-body text-center">
          <h5 class="card-title">{{titolo}}</h5>
          <h3 class="card-title">{{titoloOriginale}}</h3>
          <img :src= "'https://flagcdn.com/16x12/' + lingua + '.png'">
          <p class="card-text">{{voto}}</p>
          
      </div>
</div>
</template>

<script>
export default {
  name: 'cardFilm',
  props: ["titolo","titoloOriginale","lingua","voto"]
}
</script>


<style scoped lang="scss">

</style> 
