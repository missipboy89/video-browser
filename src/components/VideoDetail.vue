<template>
    <div v-if="video">
        <div class="details">
            <div>
                <iframe :src="videoUrl" />
            </div>
            <h4>{{ video.snippet.title }}</h4>
            <p>{{ video.snippet.description }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'VideoDetail',
    props: ['video'],
    computed: {
        videoUrl() {
            const { videoId } = this.video.id;
            return `https://www.yourube.com/embed/${videoId}`;
        }
    }
}
</script>

<style scoped>
.details {
    margin-top: 10px;
    padding: 10;
    border: 1px solid #ddd;
    border-radius: 4px;
}
</style>