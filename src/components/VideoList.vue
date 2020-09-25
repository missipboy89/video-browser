<template>
    <ul class="list-group">
        <VideoListItem 
            v-for="(video,index) in videos"
            :video="video"
            :key="index"
            @videoSelect="onVideoSelect"
        >
        </VideoListItem>
    </ul>
</template>

<script>
import VideoListItem from './VideoListItem' //test
export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    props: ['videos'],
    methods: {
        onVideoSelect(video) {
            this.$emit('videoSelect', video);
        }
    }
};
</script>

<style>

</style>