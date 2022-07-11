<template>
  <div id="app">
   <HeaderComp/>
   <main>
    <ListComponent/>
   </main>
   
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import ListComponent from './components/ListComponent.vue'


export default {
  name: 'App',
  components: {
    HeaderComp,
    ListComponent, 
  },

 
}
</script>

<style lang="scss">
@import './style/common';
@import './style/variables';
  #app{   
      height: 100vh; 
      width: 100%;    
      background-color: $brand_secondary_color;   
      overflow-y: auto;  
  }
</style>
