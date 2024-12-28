<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div class="title-bar">
        <b><RouterLink to="/">Super Link Studio</RouterLink></b>
        <div>
            <a href="https://github.com/SuperLinkStudio">Github</a>
        </div>
    </div>
    <RouterView />
</template>

<style scoped>
    .title-bar {
        position: fixed;
        display: flex;
        justify-content: space-between;
        top: 0;
        left: 0;
        right: 0;
        padding: 56px;
    }
</style>