<template>
  <div class="home">
    <h1>GIFS</h1>
      <iframe v-bind:src="gifs.data[0].embed_url"></iframe>
<!-- <p> <img v-bind:src="gifs.data[0].embed_url"></p> -->
<hr />
<hr />
<hr />
<hr />
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
        axios.get("https://api.giphy.com/v1/gifs/trending?api_key=UIQjNNyJoROGDYhOB1qGpwV2y7YEOOfM&limit=3&rating=r").then(response => {
          console.log(response.data)
          this.gifs = response.data 
        })
      }
    },
  };
</script>
