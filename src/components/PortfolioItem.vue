<script setup>
defineProps({
    images: Array
})
</script>

<template>
    <div class="project-container">
        <div class="project-text">
            <h1 class="project-title"><slot name="title">Title</slot></h1>
            <div class="project-text"><slot>Text</slot></div>
            <a href="#top">▲ gallery</a>
        </div>
        <div class="project-images-list">
           <img v-for="image in images" class="project-image" :src="'/artwork/' + image.src" :alt="image.alt" /> 
        </div>
    </div>
</template>

<style scoped>
.project-container {
    display: grid;
    padding: 20px;
    gap: 20px;
    grid-template-columns: 1fr 1fr 1fr;
}

.project-images-list {
    grid-column-end: span 2;
    display: grid;
    gap: 20px;
}

.project-image {
    width: 100%;
}

@media only screen and (max-width: 766px) {
    .project-container {
        grid-template-columns: 1fr;
    }
    .project-images-list {
        grid-column-end: span 1;
    }
}
</style>
