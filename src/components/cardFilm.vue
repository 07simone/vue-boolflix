<template>
<div>
<!-- v-if="immagineLocandina !== null"  -->
<div class="card">
      <div class="card-body text-center"> 

          <div class="img"  >
              <img  class="img-fluid" :src="'https://image.tmdb.org/t/p/w342' + immagineLocandina ">
          </div>

          <div class="description">
              <h5 class="card-title">{{titolo}}</h5>
              <h3 class="card-title">{{titoloOriginale}}</h3>
              <img :src= "'https://flagcdn.com/16x12/' + lingua + '.png'">
              <p class="card-text">{{voto}}</p>
              <p class="informazioni">{{descrizione}}</p>
              <div  class="stelle" v-for="(n) in averageGrade(voto)" :key="n">
                <h1>*</h1>
              </div>
          </div>
      </div > 
</div>


<!-- film -->
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
  props: ["titolo","titoloOriginale","lingua","voto","immagineLocandina","descrizione"],



methods:{
  averageGrade(voto){
    return parseInt (voto / 2)
  }
}
}


</script>


<style scoped lang="scss">

.img{
  width:100%
}

.description{
  display: none;
}
.card:hover{
  .card{
  height: 600px;
  }

    & .img{
      display: none;
  }
    & .description{
      display: block;
    }
  
  }

/* .img{
  display: block;
  &:hover{
    display: none;
}
}
.description{
  display: none;
  &:hover{
    display: block;
  }
} */

.stelle{
  display: inline-block;
  margin-right: 1rem;
}
</style> 
