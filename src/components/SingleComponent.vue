<template>
  <div class="text-center my-card">
        <img :src="album.poster" :alt="album.title">
        <h3>{{album.title}}</h3>
        <div>{{album.author}}</div>
        <div>{{album.year}}</div>
    </div>
</template>

<script>
export default {
    name:"SingleComponent",
    props:{
        album:Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
</style>