<template>
    <div class="main-container">
        <img class="background-logo" src="../../assets/logo.svg"
            :style="`transform: translateY(${backgroundLogoScrollY}px); opacity: ${backgroundLogoOpacity}; filter: blur(${backgroundLogoBlur}px);`" />
        <div>
            <img src="../../assets/logo.svg" />
            <div>
                <h1>Super Link Studio</h1>
                <p>超链接工作室</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.main-container {
    transition: opacity 0.1s, filter 0.1s;
    display: flex;
    flex-direction: column;
    justify-content: center;
    min-height: min(100vh, 1000px);
    animation: main-container-animation 1s ease;
    padding: 48px 16vw;
}

@keyframes main-container-animation {
    0% {
        padding: 48px 8vw;
        filter: blur(25px);
        opacity: 0;
    }
}

.background-logo {
    position: absolute;
    align-self: end;
    width: min(min(64vw, 64vh), 1000px);
}
</style>

<script lang="ts">
import { defineComponent, onMounted, onUnmounted, ref } from 'vue';

export default defineComponent({
    name: 'ScrollingBackgroundLogo',
    setup() {
        const backgroundLogoScrollY = ref(0);
        const backgroundLogoOpacity = ref(1);
        const backgroundLogoBlur = ref(2);

        const handleScroll = () => {
            const scrollDistance = window.scrollY;
            backgroundLogoScrollY.value = scrollDistance / 3.0;
            backgroundLogoOpacity.value = Math.max(0, Math.min(1, 0.1 - scrollDistance / 5000.0));
            backgroundLogoBlur.value = 24 + scrollDistance / 500.0;
        };

        onMounted(() => {
            window.addEventListener('scroll', handleScroll);
            handleScroll();
        });

        onUnmounted(() => {
            window.removeEventListener('scroll', handleScroll);
        });

        // 定义 onTouchMove 事件处理程序
        const onTouchMove = (event: TouchEvent) => {
            // 处理触摸移动事件
        };

        return {
            backgroundLogoScrollY,
            backgroundLogoOpacity,
            backgroundLogoBlur
        };
    },
});
</script>