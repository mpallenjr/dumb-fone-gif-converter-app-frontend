<template>
  <div class="home">
    <h1>{{ message }}</h1>
   <p>Keyword:    <input type="text" v-model="theKeyword"> </p>
    <button v-on:click="searchedGifs()"> SEARCH </button>
    <!-- <p> {{ results.data[0] }} </p> -->
  </div>
</template>

<style></style>

<script>
import axios from 'axios';
  export default {
    data: function () {
      return {
        message: "Dumb Fone Gif Converter",
        results: {},
        showGif: {},
        theKeyword: []
      };
    },
    created: function () {},
    methods: {
      searchedGifs: function () {
        axios.get(`https://api.giphy.com/v1/gifs/search?api_key=UIQjNNyJoROGDYhOB1qGpwV2y7YEOOfM&q=${this.theKeyword}&limit=10&offset=0&rating=r&lang=en`).then(response => {
          console.log(response.data)
          this.results = response.data 
        })
      },
    },
  };
</script>