<template>
    <ul>
        <VideoListItem v-for="video in videos" v-bind:video="video"/>
    </ul>
</template>
<script>
    import VideoListItem from "./VideoListItem";
export default {
  name: 'VideoList',
  props: ['videos'],
  components:{
    VideoListItem
  }
}
</script>
<style>

</style>
