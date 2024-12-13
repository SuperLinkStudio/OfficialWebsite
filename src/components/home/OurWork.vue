<template>
    <div class="main-container">
        <div class="title-container">
            <h1>我们的作品</h1>
            <p>OUR WORK</p>
        </div>
        <div class="card-table">
            <div class="card">
                <h3>Meanless</h3>
                <b>正 · 在 · 开 · 发</b>
            </div>
            <div class="card">
                <h3>Hyper Knowledge</h3>
                <b>正 · 在 · 开 · 发</b>
            </div>
            <div class="card">
                <h3>Hyper Authorize Platform</h3>
                <b>正 · 在 · 开 · 发</b>
            </div>
        </div>
    </div>
</template>

<style scoped>
.main-container {
    padding: 72px 16vw;
}

.title-container {
    text-align: right;
}

.card-table {
    display: grid;
    gap: 16px;
    grid-auto-flow: row;
    grid-template-columns: repeat(2, 1fr);
}

@media screen and (max-width: 1000px) {
    .card-table {
        grid-template-columns: repeat(1, 1fr);
    }
}

@media screen and (min-width: 1500px) {
    .card-table {
        grid-template-columns: repeat(3, 1fr);
    }
}

.card {
    display: block;
    background: rgb(225, 225, 225);
    min-height: min(50vh, 250px);
    box-shadow: 0 0 16px rgba(50, 50, 50, 0.1);
    padding: 16px 32px;
}
</style>