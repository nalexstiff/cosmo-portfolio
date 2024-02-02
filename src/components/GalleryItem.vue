<script setup>
    defineProps(["image", "link"])
</script>

<template>
    <a class="gallery-link" :href="'#' + link">
        <img class="gallery-image" :src="'/artwork/' + image.src" :alt="image.alt" />
    </a>
</template>

<style scoped>
.gallery-link {
    display: block;
    width: 100%;
    overflow: hidden;
    aspect-ratio: 3 / 2;
}

.gallery-image {
    width: 118%;
    margin-left: -10%;
}
</style>
