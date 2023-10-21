<template>
    <div class="text-anim" :class='{ active: isTextActive }' id="text-anim">
        <div class="container">
            <div class="text-anim__row text-anim__row--left">We unite quality professionals</div>
            <div class="text-anim__row text-anim__row--righ">with your successful bussiness</div>
        </div>
    </div>
</template>


<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const counter = ref(0);
const isTextActive = ref(false);

const startTextAnim = () => {
    const element = document.getElementById('text-anim');
    if (element) {
        const scroll = window.scrollY + window.innerHeight;
        const offset = element.offsetTop + element.offsetHeight;

        if (scroll > offset && counter.value === 0) {
            isTextActive.value = true;
            counter.value = 1;
        }
    }
};

onMounted(() => {
    window.addEventListener('scroll', startTextAnim);
    window.addEventListener('load', startTextAnim);
});

onUnmounted(() => {
    window.removeEventListener('scroll', startTextAnim);
    window.removeEventListener('load', startTextAnim);
});



</script>

<style lang="scss" scoped>
@import '../../assets/main.scss';

.text-anim {
    overflow: hidden;
    padding-bottom: 120px;

    @include min(769) {
        padding-bottom: 200px;
    }

    &.active {
        .text-anim__row {
            transform: translateX(0);
        }
    }
}

.text-anim__row {
    font-family: $font;
    font-weight: 400;
    font-style: normal;
    line-height: 1.15;
    transition: 1.5s;
    text-align: center;

    @include responsive-font(72, 40);
}

.text-anim__row--left {
    transform: translateX(-100vw);
    color: $deep-green;
}

.text-anim__row--righ {
    transform: translateX(100vw);
    background: linear-gradient(90deg, #0ad582 0%, #a2f2c0 100%);
    -webkit-background-clip: text;
    background-clip: text;

    -webkit-text-fill-color: transparent;
    text-fill-color: transparent;
}
</style>