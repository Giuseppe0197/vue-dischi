<template>
<div>
    <select @change="$emit('changeGenre', discChoice)" v-model="discChoice">
      <option value="all">tutti i generi</option>
      <option value="Rock">rock</option>
      <option value="Pop">pop</option>
      <option value="Jazz">jazz</option>
      <option value="Metal">metal</option>
  </select>
</div>
  
</template>



<script>

export default {
  name: 'Filterdisc',

  data() {
    return {
      discChoice: ""
    }
  },
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div {
    text-align: center;
    margin-bottom: 120px;

    select {
      width: 10%;
      text-align: center;
      background-color: transparent;
      color: red;
      text-transform: uppercase;
      font-weight: bold;
    }
}

</style>