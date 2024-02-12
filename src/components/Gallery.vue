<script setup>
import GalleryItem from "./GalleryItem.vue"

defineProps({
    projects: Array
})
</script>

<template>
    <div class="gallery">
        <GalleryItem v-for="project in projects" :image="project.thumb" :link="project.id" />
    </div>
</template>

<style scoped>
.gallery {
    display: grid;
    padding: 20px;
    gap: 20px;
    grid-template-columns: 1fr 1fr 1fr;
}

@media only screen and (max-width: 766px) {
    .gallery {
        grid-template-columns: 1fr 1fr;
    }
}

@media only screen and (max-width: 477px) {
    .gallery {
        grid-template-columns: 1fr;
    }
}
</style>
