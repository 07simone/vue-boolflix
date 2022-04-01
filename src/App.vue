<template>
  <div id="app">
    <IndexHeader @searchFilm="newSearch"/>,


    <IndexMain :searchTitle="string"/>
    
  </div>
</template>

<script>
import IndexHeader from './components/header.vue'
import IndexMain from './components/main.vue'

export default {
  name: 'App',
  components: {
    IndexHeader,
    IndexMain
  },
data:function(){
return{
  string: '',
}
},

  methods:{
    newSearch(searchString){
        
        this.string = searchString
    }
  
  }
}
</script>

<style lang="scss">
@import "@/style/main-style.scss";

#app {

}
</style>
