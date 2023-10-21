<template>
    <div
        class="second-slider swiper-initialized swiper-horizontal swiper-pointer-events swiper-backface-hidden"
        id="second-slider">
        <div
            class="swiper-wrapper"
            id="swiper-wrapper-3ba142c103a4c0eb4"
            aria-live="polite"
            style="transform: translate3d(0px, 0px, 0px)">
            <div
                class="swiper-slide second-slider__slide swiper-slide-active"
                style="width: 358.667px; margin-right: 80px"
                role="group"
                aria-label="1 / 3">
                <div class="second-slider__icon">
                    <img src="../../img/second-slider-icon-01.svg" alt="icon" />
                </div>
                <div class="second-slider__text">
                    We provide qualified and professional personnel - from office workers to
                    medicine personal. All types of staff what you need
                </div>
            </div>
            <div
                class="swiper-slide second-slider__slide swiper-slide-next"
                style="width: 358.667px; margin-right: 80px"
                role="group"
                aria-label="2 / 3">
                <div class="second-slider__icon">
                    <img src="../../img/second-slider-icon-02.svg" alt="icon" />
                </div>
                <div class="second-slider__text">
                    Actively recruit thousand’s of talented professionals that are unable to see
                    your job posts
                </div>
            </div>
            <div
                class="swiper-slide second-slider__slide"
                role="group"
                aria-label="3 / 3"
                style="width: 358.667px; margin-right: 80px">
                <div class="second-slider__icon">
                    <img src="../../img/second-slider-icon-03.svg" alt="icon" />
                </div>
                <div class="second-slider__text">
                    We screen candidates and handle the time-consuming work, so that you can focus
                    on hiring those who suit your needs best
                </div>
            </div>
        </div>
        <div
            class="swiper-pagination swiper-pagination-clickable swiper-pagination-bullets swiper-pagination-horizontal swiper-pagination-lock">
            <span
                class="swiper-pagination-bullet swiper-pagination-bullet-active"
                tabindex="0"
                role="button"
                aria-label="Go to slide 1"
                aria-current="true">
            </span>
        </div>
        <span class="swiper-notification" aria-live="assertive" aria-atomic="true"></span>
    </div>
</template>

<style lang="scss" scoped >
@import '../../assets/main.scss';
.second-slider {
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
//----------- Temporary ------------------------------------
.swiper-wrapper{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: auto ;
    height: auto;
    @include min(769) {
      flex-direction: row;
      justify-content: center;
    align-items: center;
    }
}


//-----------------------------------------------

.swiper-slide {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: auto !important;
    height: auto;
  }
</style>
