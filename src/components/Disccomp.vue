<template>
  <section>
      <header>
          <font-awesome-icon icon="fab fa-spotify"></font-awesome-icon>
      </header>

      <div id="container">
          <Discsubcomp/>
      </div>
      
  </section>
</template>



<script>

import Discsubcomp from '@/components/Discsubcomp.vue'
export default {
  name: 'Disccomp',
  components: {
      Discsubcomp
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

header {
    height: 60px;
    background-color: #2E3A46;

    .fa-spotify {
        color: black;
        width: 50px;
    }
}

#container {
    height: calc(100vh - 60px);
    background-color: #1E2D3B;
}
    
</style>
