<script setup>
defineProps({
    items: Array
})
</script>

<template>
    <div class="project-container">
        <div class="project-caption">
            <h1 class="project-title"><slot name="title">Title</slot></h1>
            <div class="project-text"><slot>Text</slot></div>
            <a href="#top">▲ gallery</a>
        </div>
        <div class="project-items-list">
            <template v-for="item in items">
                <div v-if="item.type == 'embed'" class="project-item embed-container" height="56.25%">
                    <iframe :src="item.url" class="project-item embed-content"></iframe>
                </div>
                <img v-if="item.type == 'image'" class="project-item" :src="'/artwork/' + item.src" :alt="item.alt" /> 
            </template>
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

.project-items-list {
    grid-column-end: span 2;
    display: grid;
    gap: 20px;
}

.project-item {
    width: 100%;
}

.embed-container {
    position: relative;
    overflow: hidden;
}

.embed-container::after {
    display: block;
    content: "";
    padding-top: 56.25%;
}

.embed-content {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
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
