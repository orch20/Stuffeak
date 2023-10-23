
import OblongBodySlider from './SliderElementsRegisterSectiin/OblongBodySlider.vue';
<template>
    <Swiper class="registr-sec__sliders" 
      
      :slidesPerView="'auto'"
      :spaceBetween="20"
      :autoplay="{
        delay: 2500,
        disableOnInteraction: false,
      }"
      
      :navigation="true"
      :modules="modules"
      @swiper="onSwiper"
      @slideChange="onSlideChange">
        <swiper-slide class="swiper-slide registr-sec__slide swiper-slide-next"><OblongBodyPicSlider /></swiper-slide>  
        <swiper-slide class="swiper-slide registr-sec__slide swiper-slide-next"><CircleBodySlider /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide swiper-slide-next"><OblongBodyPicSlider /></swiper-slide>  
        <swiper-slide class="swiper-slide registr-sec__slide swiper-slide-next"><CircleBodySlider /></swiper-slide>  
        <swiper-slide class="swiper-slide registr-sec__slide swiper-slide-next"><OblongBodyPicSlider /></swiper-slide>  
        <swiper-slide class="swiper-slide registr-sec__slide swiper-slide-next"><CircleBodySlider /></swiper-slide>    
    </Swiper>
</template>

<script setup>
import OblongBodyPicSlider from './SliderElementsRegisterSectiin/OblongBodyPicSlider.vue';
import CircleBodySlider from './SliderElementsRegisterSectiin/CircleBodySlider.vue';
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';



const onSwiper = (swiper) => {
  console.log(swiper);
};
const onSlideChange = () => {
  console.log('slide change');
};
</script>


<style scoped>
.registr-sec__sliders {
  position: relative;
  width: calc(100% + 40px);
  margin-left: -20px;

  @include min(769) {
    width: 320px;
    min-height: 70px;
    margin: 0 auto;
  }
}

.registr-sec__slider {
  overflow: hidden;
  margin-bottom: 20px;

  @include min(769) {
    position: absolute;
    top: 0;
    height: 100vh;
    margin-bottom: 0;
  }

  .swiper-wrapper {
    transition-timing-function: linear;
  }
}
</style>
