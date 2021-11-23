<template>
  <div class="home">
    <input type="text"> 
    <button v-on:click="searchGifs()"> Search </button>
    <h1> SEARCH </h1>
    <h1>TRENDING GIFS</h1>
      <iframe v-bind:src="gifs.data[0].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[1].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[2].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[3].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[4].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[5].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[6].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[7].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[8].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[9].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[10].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[11].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[12].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[13].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[14].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[15].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[16].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[17].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[18].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[19].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[20].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[21].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[22].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[23].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[24].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[25].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[26].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[27].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[28].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[29].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[30].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[31].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[32].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[33].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[34].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[35].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[36].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[37].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[38].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[39].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[40].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[41].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[42].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[43].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[44].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[45].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[46].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[47].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[48].embed_url"></iframe>
      <iframe v-bind:src="gifs.data[49].embed_url"></iframe>
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
        axios.get("https://api.giphy.com/v1/gifs/trending?api_key=UIQjNNyJoROGDYhOB1qGpwV2y7YEOOfM&limit=50&rating=r").then(response => {
          console.log(response.data)
          this.gifs = response.data 
        })
      },
      searchGifs: function () {
        console.log("search gifs")
      },
    },
  };
</script>
