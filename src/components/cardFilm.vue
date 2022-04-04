<template>
  <div class="card p-3">
        
      <div class="card-body text-center">
          <h5 class="card-title">{{nome}}</h5>
          <h3 class="card-title">{{nomeOriginale}}</h3>
          <img :src= "'https://flagcdn.com/16x12/' + linguaOriginale + '.png'">
          <p class="card-text">{{votoMedio}}</p>
          
      </div>
      <div class="card-body text-center">
          <h5 class="card-title">{{titolo}}</h5>
          <h3 class="card-title">{{titoloOriginale}}</h3>
          <!-- <img :src= "'https://flagcdn.com/16x12/' + lingua + '.png'"> -->
          <p class="card-text">{{voto}}</p>
          
      </div>
</div>
</template>

<script>
export default {
  name: 'cardFilm',
  props: ["titolo","titoloOriginale","lingua","voto","nome","nomeOriginale","linguaOriginale","votoMedio"],
  
}
</script>


<style scoped lang="scss">

</style> 
