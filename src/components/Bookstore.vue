<template>
  <div class="Bookstore">

    <div v-for="(book, index) in bookList" v-bind:key="index">
      <SingleBook v-bind:singleBook="book"></SingleBook>
    </div>

  </div>
</template>

<script>
import SingleBook from "@/components/SingleBook.vue";

export default {
  name: 'Bookstore',
  props: ["bookList"],
  components: {
   SingleBook
  },
  data(){
    return {
      // BookList:[]
    }
  },
  methods: {
    // display all books
  },
  created(){
    console.log(this.bookList)
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
