<template>
  <div>
    <SearchBar @termChange="onTermChange"> </SearchBar>
  </div>
</template>
<script>
import SearchBar from "./components/SearchBar";
const API_KEY = 'API_KEY_HERE';

export default {
  name: "App",
  components: {
    SearchBar
  },
  methods:{
    onTermChange(searchTerm){
      console.log(searchTerm);
    }
  }
};
</script>
