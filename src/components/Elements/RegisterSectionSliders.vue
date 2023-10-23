
import OblongBodySlider from './SliderElementsRegisterSectiin/OblongBodySlider.vue';
<template>
    <div class="registr-sec__sliders">
    
    <Swiper class="registr-sec__slider registr-sec__slider-01" :modules="modules" :grabCursor= false :slidesPerView="'auto'" :spaceBetween="20" :freeMode= true :reeModeMomentum= true :loop= true :speed= 6000 :mousewheelControl= false :autoplay="autoplay" :breakpoints="breakpoints" :navigation="true">
        <swiper-slide class="swiper-slide registr-sec__slide"><OblongBodyPicSlider /></swiper-slide> 
        <swiper-slide class="swiper-slide registr-sec__slide"><OblongBodyPicSlider /></swiper-slide> 
        <swiper-slide class="swiper-slide registr-sec__slide"><GreenSearchIconCircleBodySlider /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide"><GreenCircleBodySlider /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide"><OblongBodyPicSlider /></swiper-slide>  
        <swiper-slide class="swiper-slide registr-sec__slide"><GreenCircleBodySlider /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide"><OblongBodyPicSlider /></swiper-slide>  
        <swiper-slide class="swiper-slide registr-sec__slide"><GreenSearchIconCircleBodySlider /></swiper-slide>
      </Swiper>
    </div>
    
</template>

<script setup>
import OblongBodyPicSlider from './SliderElementsRegisterSection/OblongBodyPicSlider.vue';
import GreenSearchIconCircleBodySlider from './SliderElementsRegisterSection/GreenSearchIconCircleBodySlider.vue';
import GreenCircleBodySlider from './SliderElementsRegisterSection/GreenCircleBodySlider.vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Autoplay, Pagination } from 'swiper/modules';

const modules = [Autoplay, Pagination];
const autoplay = {
  delay: 1,
  disableOnInteraction: true,
}
const breakpoints = {
  769: {
    direction: "vertical",
  },
}


</script>


<style lang="scss">
@import '../../assets/main.scss';

.registr-sec__sliders {
  position: relative;
  width: calc(100% + 40px);
  margin-left: -20px;

  @include min(769) {
    width: 320px;
    min-height: 700px;
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
.registr-sec__slide {
  display: flex;
  justify-content: space-between;
  width: auto;
  min-width: 244px;
  height: 112px;
  border-radius: 56px;

  @include min(769) {
    display: block;
    width: 150px;
    min-width: 0;
    height: 320px;
    border-radius: 75px;
  }
}
.registr-sec__slider-01 {
  @include min(769) {
    left: 0;
  }
}
</style>
