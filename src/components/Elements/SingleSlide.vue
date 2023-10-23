<template>
    <div class="swiper-slide registr-sec__slide">
        <div :class="'registr-sec__slide-body registr-sec__slide-body--' + className">
            <div class="registr-sec__circle" :style="'background-color: ' + color">
                <svg width="53" height="19" viewBox="0 0 53 19" xmlns="http://www.w3.org/2000/svg">
                    <path :d=" svgPath " fill="#A2F2C0" />
                </svg>
            </div>
            <div class="registr-sec__slide-text">{{ text }}</div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        color: String,
        className: String,
        svgPath: String,
        text: String,
    },
};
</script>