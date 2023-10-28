<template>
    <section class="job-opport-sec container">
        <h2 class="job-opport-sec__main-title"><span class="italic">Latest</span> 10 job oportunities</h2>
        <div>
            <p class="job-opport-sec__city-name">City:</p>
        </div>
        <swiper :navigation="navigation" :modules="modules" :space-between="20" slides-per-view="1.2" :breakpoints="breakpoints">
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
            <swiper-slide><JobCard /></swiper-slide>
        </swiper>
        <div class="job-opport-sec__button-section">
            <div class="job-opport-sec__button-wrapper">
                <div class="job-opport-sec__button button-prev">
                
    </div>
    <div class="job-opport-sec__button button-next">
                
                </div>
            </div>
            <a href="#" class="job-opport-sec__button-section-text">See all job oportunities</a>
        </div>
    </section>
</template>

<script setup>
import JobCard from '../Elements/JobCard.vue';

import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
// import 'swiper/css';

import 'swiper/css/navigation';

// import './style.css';

// import required modules
import { Navigation } from 'swiper/modules';

const modules = [Navigation]
const navigation = {
    navigation: true,
    nextEl: '.button-next',
    prevEl: '.button-prev',
}

const breakpoints = {
    600: {
        slidesPerView: 2.2,
    },
    1025: {
        slidesPerView: 3.2,
    },
    1200: {
        slidesPerView: 4,
    },
}

</script>

<style lang="scss">
@import '../../assets/main.scss';

.swiper-button-prev::after,
.swiper-button-next::after {
  display: none;
}

.job-opport-sec__button{
    cursor: pointer;
    display: inline-block;
    width: 60px;
    height: 60px;
    background-color: $main-green;
}

.button-next {
   
    -webkit-mask: url('../../img/arr-right-in-the-circle.svg') no-repeat 100% 100%;
    mask: url('../../img/arr-right-in-the-circle.svg') no-repeat 100% 100%;
    -webkit-mask-size: cover;
    mask-size: cover;
}

.button-prev {
    
    -webkit-mask: url('../../img/arr-left-in-the-circle.svg') no-repeat 100% 100%;
    mask: url('../../img/arr-left-in-the-circle.svg') no-repeat 100% 100%;
    -webkit-mask-size: cover;
    mask-size: cover;
    
}

.button-next.swiper-button-disabled,
.button-prev.swiper-button-disabled {
    background-color: #014750;
    opacity: 0.25;
}



.job-opport-sec{
    padding: 60px 0 50px 15px;
    
}
.job-opport-sec__main-title{
    font-family: $font;
    font-weight: 500;
    font-style: normal;
    line-height: 1.1;
    max-width: 600px;
    margin-bottom: auto;
    user-select: none;
    color: $dark-green;
    margin-bottom: 22px;
}

.job-opport-sec__city-name{
    font-family: $font;
    font-size: 12px;
    font-weight: 500;
    font-style: normal;
    line-height: 1.1;
    color: $dark-green;
    margin-bottom: 30px;
}


.job-opport-sec__button-section{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 15px;
}

.job-opport-sec__button-wrapper{
    display: flex;
    gap: 10px;
    margin-right: auto;

}

.job-opport-sec__button-section-text{
    font-family: $font;
    font-size: 16px;
    font-weight: 600;
    font-style: normal;
    line-height: 1.1;
    color: $dark-green;
}

</style>