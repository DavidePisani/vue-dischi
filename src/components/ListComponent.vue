<template>
<section>
    <div class="container"> 
        <div class="d-flex justify-center">
            <SearchBar @SearchGenre="GenreMusic"/>
        </div>

        <div class=" text-center row row-cols-5">
             <div class="col" v-for="album, index in SelectMusic" :key="index">
                <SingleComponent :music="album"/>
            </div>
        </div>
    </div>
</section>
</template> 
<script>
import SingleComponent from './SingleComponent.vue'
import SearchBar from './SearchBar.vue'
import axios from 'axios';
export default {
    name:'ListComponent',
    components:{
        SingleComponent,
        SearchBar,
    },
    

    data(){
        return{
            url: "https://flynn.boolean.careers/exercises/api/array/music",
            albumArrey:[],
            musicValue:''  
        }
    },

    computed:{
        SelectMusic(){
            if(this.musicValue === 'All'){
                return this.albumArrey
            }else{
                return this.albumArrey.filter((music)=> {
                    return music.genre.includes(this.musicValue) || music.author.includes(this.musicValue) ;
                });  
            }               
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
    },

   
    GenreMusic(value){
        this.musicValue = value
    }
    
  }
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
    section{
        // background-color: $brand_secondary_color;
        // height:calc(100vh - 60px);

        .col{
            margin: 15px 0;
        }
    }
</style>