<template>
    <div :style="{ width: width, height: height }" ref="container"></div>
</template>

<script setup>
import { onMounted, onBeforeUnmount, ref } from 'vue';
import lottie from 'lottie-web';

const props = defineProps({
    path: {
        type: String,
        required: true
    },
    width: {
        type: String,
        default: '100%'
    },
    height: {
        type: String,
        default: '100%'
    },
    speed: {
        type: Number,
        default: 1
    }
});

const container = ref(null);
let animation = null;

onMounted(async () => {
    const animationData = await fetch(props.path).then(r => r.json());
    
    animation = lottie.loadAnimation({
        container: container.value,
        renderer: 'svg',
        loop: true,
        autoplay: true,
        animationData
    });

    animation.setSpeed(props.speed);
});

onBeforeUnmount(() => {
    if (animation) {
        animation.destroy();
    }
});
</script> 