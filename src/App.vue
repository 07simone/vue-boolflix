<template>
  <div id="app">
    <IndexHeader/>,


    <IndexMain/>
    
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
  }
}
</script>

<style lang="scss">
@import "@/style/main-style.scss";

#app {

}
</style>
