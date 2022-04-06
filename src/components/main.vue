<template>
<main>

<div class="container">
  <div  class="row row-cols-3 mt-5 g-5 ">
        <div  class="col" v-for="(element,index) in searchTv " :key="index +'serie'" >
            <cardFilm
              :titolo="element.name"
              :immagineLocandina="element.poster_path"
              :titoloOriginale="element.original_name"
              :lingua="element.original_language"
              :descrizione="element.overview"
              :voto="element.vote_average"
              
            />
        </div>
  </div>
  <div  class="row row-cols-3 mt-5 g-5 ">
      <div  class="col" v-for="(element,index) in searchmovie" :key="index">
          <cardFilm
            :titolo="element.original_title"
            :immagineLocandina="element.poster_path"
            :titoloOriginale="element.original_title"
            :lingua="element.original_language"
            :descrizione="element.overview"
            :voto="element.vote_average"
            
          />
      </div>
    </div> 

</div>





</main>
</template>

<script>

import cardFilm from './cardFilm.vue'

export default {
  name: 'IndexMain',
  props:{ 'searchmovie' : Array, 'searchTv' : Array  },   // il dato ricevuto attraverso i props da app.vue

  components:{
    cardFilm,
  
  },


  data:function(){
    return{
    
    
    }
  },
  

  methods:{

  }
}
</script>


<style scoped lang="scss">

</style>
