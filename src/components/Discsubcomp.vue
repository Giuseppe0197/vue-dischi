<template>

    <div class="discs">

      <img :src="details.poster">

      <h3 class="titleDisc">{{details.title}}</h3>

      <p>

        <span>{{details.author}}</span>
        <span>{{details.year}}</span>

      </p>

    </div>

</template>

<script>
export default {
  name: 'Discsubcomp',

  props: {
    details: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">



  .discs {
    width: calc(100% / 5 - 30px);
    min-height: 350px;
    background-color: #2E3A46;
    text-align: center;
    margin-bottom: 30px;
    
    img {
      max-width: 80%;
      margin-top: 20px;
      
    }

    h3 {
      color: white;
      font-size: 25px;
      margin-top: 15px;
    }

    p {
      margin-top: 20px;

      span {
        display: block;
        color: #867D75;
      }

    }

  }

</style>
