<template>
  <div class="index">
    <h1>TRENDING GIFS</h1>
      <iframe v-for="gif in gifs.data" v-bind:src="gif.embed_url"></iframe>
      
  </div>
</template>

<style></style>

<script>
import axios from 'axios';
  export default {
    data: function () {
      return {
        gifs: {},
      };
    },
    created: function () {
      this.indexGifs();
    },
    methods: {
      indexGifs: function () {
        console.log('hello')
        axios.get("https://api.giphy.com/v1/gifs/trending?api_key=UIQjNNyJoROGDYhOB1qGpwV2y7YEOOfM&limit=50&rating=r").then(response => {
          console.log(response.data)
          this.gifs = response.data 
        })
      },
    },
  };
</script>
