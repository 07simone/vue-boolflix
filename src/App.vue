<template>
  <div id="app">
    <IndexHeader @searchFilm="newSearch"/>      <!-- //sono in attesa di un evento searchfilm, quando viene chiamato allora chiamami newsearch -->


    <IndexMain :searchTv="searchTv" :searchTitle="searchTitle" />           <!-- per comunicare con il figlio main -->
    
  </div>
</template>

<script>
import axios from 'axios';
import IndexHeader from './components/header.vue';
import IndexMain from './components/main.vue';

export default {
  name: 'App',
  components: {
    IndexHeader,
    IndexMain
  },
data:function(){
return{
  searchTitle: [],
  searchTv:[]
}
},

  methods:{
    newSearch(searchFilm){
      axios.get(`https://api.themoviedb.org/3/search/movie?api_key=9d2431df25d8fce1b879e42ed15638d1&language=it&query=${searchFilm}`)
        .then((risultato)=>{
          this.searchTitle = risultato.data.results
          console.log(this.searchTitle)
        })
        .catch((errore) =>{
          console.log(errore)
        })

      axios.get(`https://api.themoviedb.org/3/search/tv?api_key=9d2431df25d8fce1b879e42ed15638d1&language=it&query=${searchFilm}`)
        .then((risultato)=>{
          this.searchTv = risultato.data.results
          console.log(this.searchTv)
        })
        .catch((errore) =>{
          console.log(errore)
        })
    },
  
  }
}
</script>

<style lang="scss">
@import "@/style/main-style.scss";
@import "./style/partials/_variables.scss";


/* #app {

} */
</style>
