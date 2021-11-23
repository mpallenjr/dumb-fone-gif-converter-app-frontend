<template>
  <div class="home">
    <h1>GIFS</h1>
    <div v-for="gif in gifs">
<p> {{ gifs.data[0].url }} </p>
<hr />
<hr />
<hr />
<hr />
</div> 
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
        axios.get("https://api.giphy.com/v1/gifs/trending?api_key=UIQjNNyJoROGDYhOB1qGpwV2y7YEOOfM&limit=10&rating=r").then(response => {
          console.log(response.data)
          this.gifs = response.data 
        })
      }
    },
  };
</script>
