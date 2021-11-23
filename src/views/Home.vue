<template>
  <div class="home">
    <h1>GIFS</h1>

  </div>
</template>

<style></style>

<script>
import axios from 'axios';
  export default {
    data: function () {
      return {
        
      };
    },
    created: function () {
      this.indexGifs();
    },
    methods: {
      indexGifs: function () {
        console.log('hello')
        axios.get("https://api.giphy.com/v1/gifs/trending?api_key=UIQjNNyJoROGDYhOB1qGpwV2y7YEOOfM&limit=10&rating=r").then(response => {
          console.log(response.data)
        })
      }
    },
  };
</script>
