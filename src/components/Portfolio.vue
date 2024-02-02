<script setup>
import PortfolioItem from "./PortfolioItem.vue"

defineProps({
    projects: Array
})
</script>

<template>
    <div class="portfolio-container">
        <PortfolioItem v-for="project in projects" :id="project.id" :images="project.images">
            <template #title>{{ project.title }}</template>
            <p v-for="para in project.text">{{ para }}</p>
        </PortfolioItem>
    </div>
</template>

<style scoped>
</style>
