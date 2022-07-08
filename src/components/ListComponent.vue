<template>
<section>
    <div class="container">
            <div class="row row-cols-5">
                <div class="col gy6" v-for="album, index in albumArrey" :key="index">
                    <SingleComponent :music="album"/>
                </div>
            </div>
        </div>
</section>
</template> 
<script>
import SingleComponent from './SingleComponent.vue'
import axios from 'axios';
export default {
    name:'ListComponent',
    SingleComponent,

    data(){
        return{
            url: "https://flynn.boolean.careers/exercises/api/array/music",
            albumArrey:[],
        }
    },
    created(){
        this.getElement()
    },


 methods:{
    getElement(){
      axios.get(this.url).then((result)=> {
        this.albumArrey = result.data.response
      })
      .catch((err)=>{
        console.log(err)
      })
    }
    
  }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
    section{
        background-color: $brand_secondary_color;
        height: 100%;
        padding: 30px;
    }
.my-card{
    background-color:$brand_primary_color;
    width: 100%;
    margin: 0 auto;
    padding: 20px;
    
    img{
        width: 100%;
    }

    h3{
        color: $primary_text;
    }

    div{
        color:$secondary_text
    }

}

</style>