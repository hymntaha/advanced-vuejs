<template>
    <ul>
        VideoList
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
