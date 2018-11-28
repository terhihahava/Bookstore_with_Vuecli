<template>
  <div id="app">

    <div v-if="isLoading">
      <p>Loading ...</p>
    </div>

    <div v-else>
      <Bookstore v-bind:bookList="this.allBooks"></Bookstore>
    </div>

  </div>
</template>

<script>
import Bookstore from "@/components/Bookstore.vue";
export default {
  name: 'app',
  components: {
    Bookstore
  },
  data() {
    return {
      allBooks: [],
      isLoading: true
    }
  },
  created() {
    var url = "https://api.myjson.com/bins/udbm5";

    fetch(url)
      .then(function (response) {
          //    console.log(response) ("Request succeeded")
          return response.json();
      })
      .then(json => {
        this.allBooks = json.books
        console.log(this.allBooks)
        this.isLoading = false
      })
  }
  
}
</script>

<style>

</style>
