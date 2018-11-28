<template>
  <div class="flipCard">

   
    <div class="flipCardFront">

      <img v-bind:src="singleBook.portada" />
      
    </div>

    <div class="flipCardBack">

      <h1> {{singleBook.titulo}} </h1>
      <p> {{singleBook.descripcion}}</p>
      <!-- <button class=myButton> 
       v-on:click="">Read more</button> -->
     </div>

   </div>
</template>

<script>
export default {
  name: 'SingleBook',
  props: ["singleBook"],
  
  data(){
    return {
      
    }
  },
  methods: {
  
  },
  created(){
    // console.log(this.singleBook)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
