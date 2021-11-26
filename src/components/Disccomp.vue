<template>
  <section>
      <header>

        <i class="fab fa-spotify"></i>

      </header>

      <div id="container">

        <LoaderPage v-if="discList.length === 0"/>

        <div v-else id="containerDiscs">
        <Discsubcomp
        v-for="disc, i in discList" 
        :key="i"
        :details="disc"
        />
        </div>

      </div>
      
  </section>
</template>



<script>

import axios from "axios";
import Discsubcomp from '@/components/Discsubcomp.vue';
import LoaderPage from '@/components/LoaderPage.vue';


export default {
  name: 'Disccomp',
  components: {
      Discsubcomp,
      LoaderPage
  },

  data() {
      return {
          apiUrl: "https://flynn.boolean.careers/exercises/api/array/music",

          discList: []
      }
  },

  created() {
      this.getdiscSpot()
  },

  methods: {
      getdiscSpot() {

        axios
        .get(this.apiUrl)
        .then((result) => {
            
            this.discList = result.data.response

        })
        
      }
  }
  
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

header {
    height: 60px;
    background-color: #2E3A46;
    

    .fa-spotify {
        color: #1ED760;
        font-size: 40px;
        /* vertical-align: middle; */
        line-height: 60px;
        margin-left: 10px;
    }
}

#container {
    height: calc(100vh - 60px);
    background-color: #1E2D3B;
    overflow-y: scroll;

    #containerDiscs {
        width: 70%;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        margin-top: 40px;
    }
}
    
</style>
