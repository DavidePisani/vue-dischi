<template>
  <div class="text-center my-card">
        <img :src="music.poster" :alt="music.title">
        <h3>{{music.title}}</h3>
        <div>{{music.author}}</div>
        <div>{{music.year}}</div>
    </div>
</template>

<script>
export default {
    name:"SingleComponent",
    props:{
        music:Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';

.my-card{
    background-color:$brand_primary_color;
    height: 100%;
    padding: 20px;

    
    img{
        width: 100%;
    }

    h3{
        color: $primary_text;
        font-size: 20px;
        padding-top: 30px;
    }

    div{
        color:$secondary_text
    }
}
</style>