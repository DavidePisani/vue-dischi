<template>
<section>
    <div class="container">
            <div class="row row-cols-5">
                <div class="col" v-for="album, index in albumArrey" :key="index">
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
    components:{
        SingleComponent,
    },
    

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
        height:calc(100vh - 60px) ;
        
        .col{
            margin: 15px 0;
        }
    }
</style>