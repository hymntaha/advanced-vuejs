<template>
  <div class="container">
    <SearchBar @termChange="onTermChange"> </SearchBar>
    <VideoList @videSelect="onVideoSelect" :videos="videos"/>

  </div>
</template>
<script>
import SearchBar from "./components/SearchBar";
import VideoList from "./components/VideoList";

import axios from 'axios';
const API_KEY = 'API_KEY_HERE';

export default {
  name: "App",
  components: {
    SearchBar,
    VideoList
  },
  data(){
    return { videos:[]};
  },
  methods:{
    onVideoSelect(video){
      console.log(video);
    },
    onTermChange(searchTerm){
      axios.get('https://www.googleapis.com/youtube/v3/search', {
        params: {
          keY: API_KEY,
          type: 'video',
          part: 'snippet',
          q: searchTerm
        }
      }).then(response => {
        this.videos = response.data.items;
      });
    }
  }
};
</script>
