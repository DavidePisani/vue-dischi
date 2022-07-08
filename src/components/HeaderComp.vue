<template>
  <header>
    <img src="../assets/logo-small.svg" alt="">
  </header>

</template>

<script>
export default {
  name:'HeaderComp'

}
</script>

<style lang="scss" scoped>

@import '../style/variables';

    header{
        background-color: $brand_primary_color ;
        height: 60px;
        padding: 10px;

        img{
            height: 100%;
        }

    }

</style>