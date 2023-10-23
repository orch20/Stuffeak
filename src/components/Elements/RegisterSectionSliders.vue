
import OblongBodySlider from './SliderElementsRegisterSectiin/OblongBodySlider.vue';
<template>
    <div class="registr-sec__sliders">
      <Swiper class="registr-sec__slider registr-sec__slider-01" :modules="modules" :grabCursor= false :slidesPerView="'auto'" :spaceBetween="20" :freeMode= true :reeModeMomentum= true :loop= true :speed= 6000 :mousewheelControl= false :autoplay="autoplayLeft" :breakpoints="breakpoints" :navigation="true">
        <swiper-slide class="swiper-slide registr-sec__slide"><Icon247andManSlider /></swiper-slide> 
        <swiper-slide class="swiper-slide registr-sec__slide"><PicAndITSlider /></swiper-slide> 
        <swiper-slide class="swiper-slide registr-sec__slide"><GreenCircleAndIconSearchCircle /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide"><PicAndNursingSliderDarker /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide"><Icon247andManSlider /></swiper-slide> 
        <swiper-slide class="swiper-slide registr-sec__slide"><PicAndITSlider /></swiper-slide> 
        <swiper-slide class="swiper-slide registr-sec__slide"><GreenCircleAndIconSearchCircle /></swiper-slide>
        <swiper-slide class="swiper-slide registr-sec__slide"><PicAndNursingSliderDarker /></swiper-slide>
      </Swiper>
      <Swiper class="registr-sec__slider registr-sec__slider-02" :modules="modules" :grabCursor= false :slidesPerView="'auto'" :spaceBetween="20" :freeMode= true :reeModeMomentum= true :loop= true :speed= 6000 :mousewheelControl= false :autoplay="autoplayRight" :breakpoints="breakpoints" :navigation="true">
          <swiper-slide class="swiper-slide registr-sec__slide"><Icon247andManSlider /></swiper-slide> 
          <swiper-slide class="swiper-slide registr-sec__slide"><PicAndITSlider /></swiper-slide> 
          <swiper-slide class="swiper-slide registr-sec__slide"><GreenCircleAndIconSearchCircle /></swiper-slide>
          <swiper-slide class="swiper-slide registr-sec__slide"><PicAndNursingSliderDarker /></swiper-slide>
          <swiper-slide class="swiper-slide registr-sec__slide"><Icon247andManSlider /></swiper-slide> 
          <swiper-slide class="swiper-slide registr-sec__slide"><PicAndITSlider /></swiper-slide> 
          <swiper-slide class="swiper-slide registr-sec__slide"><GreenCircleAndIconSearchCircle /></swiper-slide>
          <swiper-slide class="swiper-slide registr-sec__slide"><PicAndNursingSliderDarker /></swiper-slide>
        </Swiper>
    
    </div>
</template>

<script setup>
import Icon247andManSlider from './SliderElementsRegisterSection/Icon247andManSlider.vue';
import PicAndITSlider from './SliderElementsRegisterSection/PicAndITSlider.vue';
import GreenCircleAndIconSearchCircle from './SliderElementsRegisterSection/GreenCircleAndIconSearchCircle.vue';
import PicAndNursingSliderDarker from './SliderElementsRegisterSection/PicAndNursingSliderDarker.vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Autoplay, Pagination } from 'swiper/modules';

const modules = [Autoplay, Pagination];
const autoplayLeft = {
  delay: 1,
  disableOnInteraction: true,
}
const autoplayRight = {
  delay: 1,
  disableOnInteraction: true,
  reverseDirection: true,
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

.registr-sec__slider-02 {
  @include min(769) {
    right: 0;
  }
}
</style>
