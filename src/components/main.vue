<template>
<main>

<div class="container">
    <div class="row row cols-5 mb-5">
      <div class="col" v-for="(element,index) in newFilm(searchTitle)" :key="index">
          <listaFilm
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
import axios from 'axios'
import listaFilm from './listaFilm.vue'

export default {
  name: 'IndexMain',
  props:{ 'searchTitle' : String },
  components:{
    listaFilm,
  },


  data:function(){
    return{
      IndexMain: null,
    }
  },
  created: function(){
    this.libraryFilm();
  },

  methods:{

    newFilm(searchfilms){
      /* sovrascrivi indexmain con la nuova lista dei film con il nome cercato */
      return  this.IndexMain.filter(
        (elemento) =>  (elemento.original_title.toLowerCase().includes(searchfilms.toLowerCase())) 
          )
    },

    libraryFilm(){
      axios.get("https://api.themoviedb.org/3/search/movie?api_key=9d2431df25d8fce1b879e42ed15638d1&language=en-US&page=1&include_adult=false&query=2")
      .then((risultato)=>{
        console.log(risultato)
        this.IndexMain = risultato.data.results
      })
      .catch((errore) =>{
        console.log(errore)
      })
    }
  }
}
</script>


<style scoped lang="scss">

</style>
