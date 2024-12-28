<template>
    <div class="main-container">
        <h2>我们是开发者、艺术家、胸怀大志的青年</h2>
        <h3>一个年轻的开发团队，无数个天马行空的狂想</h3>
        <p class="backdrop-text">Shape the world into what we desire</p>
    </div>
</template>

<style scoped>
.main-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 16px 16vw 144px;
}

.main-container * {
    margin: 4px;
    text-align: center;
}

.backdrop-text {
    position: absolute;
    zoom: 3;
    font-weight: 900;
    opacity: 0.2;
    filter: blur(1px);
    padding: 16%;
    z-index: -1;
}
</style>