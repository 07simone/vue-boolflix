<template>
<div>

  <!-- film -->
  <div class="card p-3">
      <div  class="card-body text-center">
          <h5 class="card-title">{{titolo}}</h5>
          <img v-if="immagineLocandina !== null" class="locandina" :src="'https://image.tmdb.org/t/p/w200' + immagineLocandina ">
          <h3 class="card-title">{{titoloOriginale}}</h3>
          <img :src= "'https://flagcdn.com/16x12/' + lingua + '.png'">
          <p class="card-text">{{voto}}</p>
          <div class="stelle" v-for="(n) in mediaVoto(voto)" :key="n">
            <h1>*</h1>
          </div>
          
      </div>
</div>

<!-- serietv -->
  <!-- <div class="card p-3">
    <div  class="card-body text-center">
          <h5 class="card-title">{{titolo}}</h5>
          <img class="locandina " :src="'https://image.tmdb.org/t/p/w200' + immagine">
          <h3 class="card-title">{{titoloOriginale}}</h3>
          
          <p class="card-text">{{voto}}</p>
      </div> 
  </div>  -->
    

</div>

</template>

<script>
export default {
  name: 'cardFilm',
  props: ["titolo","titoloOriginale","lingua","voto","immagineLocandina"],


methods:{
  mediaVoto(voto){
    return parseInt (voto/ 2)
  }
}
}


</script>


<style scoped lang="scss">
.locandina{
  width: 100%;
}

.stelle{
  display: inline-block;
  margin-right: 1rem;
}
</style> 
