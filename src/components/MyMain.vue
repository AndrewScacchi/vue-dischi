<template>
    <div id="main">
      <div id="container">
        <SelectorOpt
        @mySearch="inputGenre"
        />
        
        
        
        <MusicCard
                v-for="(item, i) in filteredGenre"
                :key="i"
                :albumObj="item"
            /> 
        
      </div>
        
    </div>
</template>

<script>
import MusicCard from './MusicCard.vue'
import axios from "axios"
import SelectorOpt from "./SelectorOpt.vue"


export default {
  name: 'MyMain',
  components: {
      MusicCard,
      SelectorOpt
  },
  data() {
      return {
          apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",
          albumList: [],
          userText : "",
      }
  },
  created() {
      this.getAlbum();
  },
  methods: {
      getAlbum() {
          axios
              .get(this.apiUrl)
              .then((result) => {
                  this.albumList = result.data.response;
              })
              .catch((error) => {
                  console.log("Errore", error);
              })
      },
       inputGenre(userGenre) {
            this.userText = userGenre;
        }
    },
    computed: {
        filteredGenre(){
            if ( this.userText === "all") {
                return this.albumList;
            }   else {
                return this.albumList.filter(item => {
                    return item.genre.toLowerCase().includes(this.userText.toLowerCase());
                });
            }
        }
    }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  #main {
    width: 100%;
    // height: calc(100vh - 50px);
    height: 100vh;
    background-color: #1e2d3b;
    padding: 25px 0;
  }
  #container{
    width: 80%;
    margin: 0 auto;
    // border: 1px solid red;
    // min-height: 400px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

  }
</style>
