<template>

  <swiper class="second-slider" :modules="modules" :space-between="0" slides-per-view="1" :pagination="pagination" :breakpoints="breakpoints">
      <swiper-slide>
        <div class="second-slider__icon">
            <img src="../../img/second-slider-icon-01.svg" alt="icon" />
        </div>
        <div class="second-slider__text">
            We provide qualified and professional personnel - from office workers to
            medicine personal. All types of staff what you need
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="second-slider__icon">
          <img src="../../img/second-slider-icon-02.svg" alt="icon" />
        </div>
        <div class="second-slider__text">
            Actively recruit thousand’s of talented professionals that are unable to see
            your job posts
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="second-slider__icon">
          <img src="../../img/second-slider-icon-03.svg" alt="icon" />
          </div>
          <div class="second-slider__text">
              We screen candidates and handle the time-consuming work, so that you can focus
              on hiring those who suit your needs best
          </div>
      </swiper-slide>
      <div class="swiper-pagination"></div>
    </swiper>
</template>


<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Pagination } from 'swiper/modules';

const modules = [Pagination];

const pagination = {
  clickable: true,
  el: ".swiper-pagination",
}
const breakpoints = {
  600: {
    spaceBetween: 30,
    slidesPerView: 2,
  },
  1025: {
    spaceBetween: 40,
    slidesPerView: 3,
  },
  1200: {
    spaceBetween: 80,
    slidesPerView: 3,
  },
}
</script>



<style lang="scss">
@import '../../assets/main.scss';

.second-slider {
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
  padding-bottom: 80px;

  .swiper-pagination {
    bottom: 30px;
    text-align: left;
  }

  .swiper-pagination-bullet {
    background-color: $light-grey;
  }

  .swiper-pagination-bullet-active {
    background-color: $main-green;
    
  }
}

.second-slider__icon {
  margin-bottom: 50px;

  img {
    display: block;
    max-width: 100%;
  }
}

.second-slider__text {
  font-family: $font;
  font-size: 18px;
  font-weight: 500;
  font-style: normal;
  line-height: 22px;
  color: $neutral-white;
}

</style>
