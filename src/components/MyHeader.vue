<template>
  <section>
      <header>

        <i class="fab fa-spotify"></i>

        <!-- <Filterdisc/> -->

        <div id="listadischi">
            <select @change="$emit('changeGenre', discChoice)" v-model="discChoice">
            <option value="all">tutti i generi</option>
            <option value="Rock">rock</option>
            <option value="Pop">pop</option>
            <option value="Jazz">jazz</option>
            <option value="Metal">metal</option>
            </select>
        </div>

      </header>

  </section>
</template>



<script>

/* import Filterdisc from '@/components/Filterdisc.vue'; */


export default {
  name: 'MyHeader',
  components: {
      /* Filterdisc */
  },

  props: {
      genres: Array
  },

  data() {
    return {
      discChoice: ""
    }
  },

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
        line-height: 60px;
        margin-left: 10px;
    }

    #listadischi {
    float: right;
    margin-top: 20px;
    margin-right: 20px;

    select {
      width: 20%;
      text-align: center;
      background-color: transparent;
      color: red;
      text-transform: uppercase;
      font-weight: bold;

      option {
        background-color: #2E3A46;
      }
    }
}
}
    
</style>
