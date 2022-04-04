<template>
<main>

<div class="container">
    <div class="row row-cols-5 mb-5">
      <div class="col" v-for="(element,index) in searchTv" :key="index">
          <cardFilm
            :nome="element.name"
            :nomeOriginale="element.original_name"
            :linguaOriginale="element.original_language"
            :votoMedio="element.vote_averege"
            
          />
      </div>
      <div class="col" v-for="(element,index) in searchTitle" :key="index">
          <cardFilm
            :titolo="element.original_title"
            :titoloOriginale="element.original_title"
            :lingua="element.original_language"
            :voto="element.vote_averege"
            
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
  props:{ 'searchTitle' : Array, 'searchTv' : Array  },   // il dato ricevuto attraverso i props da app.vue
                  
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
main{
  background-color: "$bgcolor";
}
</style>
