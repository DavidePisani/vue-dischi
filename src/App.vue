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

</style>
