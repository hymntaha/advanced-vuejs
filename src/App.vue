<template>
  <div>
    <SearchBar @termChange="onTermChange"> </SearchBar>
  </div>
</template>
<script>
import SearchBar from "./components/SearchBar";
import axios from 'axios';
const API_KEY = 'API_KEY_HERE';

export default {
  name: "App",
  components: {
    SearchBar
  },
  methods:{
    onTermChange(searchTerm){
      axios.get('https://googleapis.com/youtube/v3/search')
    }
  }
};
</script>
