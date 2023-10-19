<template>
    <div class="second">
        <div class="second__inn"></div>
            <div class="container">
            <h2 class="second__title">What makes us <span class="italic">different</span> from the others?</h2>
            
                <div class="second-slider swiper-initialized swiper-horizontal swiper-backface-hidden" id="second-slider">
                    <div class="swiper-wrapper" id="swiper-wrapper-8aaed5fee2b5dec7" aria-live="polite" style="transform: translate3d(0px, 0px, 0px);">
                    <div class="swiper-slide second-slider__slide swiper-slide-active" role="group" aria-label="1 / 3" style="width: 360px; margin-right: 80px;">
                        <div class="second-slider__icon"><img src="../../img/second-slider-icon-01.svg" alt="icon"></div>
                        <div class="second-slider__text">We provide qualified and professional personnel - from office workers to medicine personal. All types of staff what you need</div>
                    </div>
                    <div class="swiper-slide second-slider__slide swiper-slide-next" role="group" aria-label="2 / 3" style="width: 360px; margin-right: 80px;">
                        <div class="second-slider__icon"><img src="../../img/second-slider-icon-02.svg" alt="icon"></div>
                        <div class="second-slider__text">Actively recruit thousand’s of talented professionals that are unable to see your job posts</div>
                    </div>
                    <div class="swiper-slide second-slider__slide" role="group" aria-label="3 / 3" style="width: 360px; margin-right: 80px;">
                        <div class="second-slider__icon"><img src="../../img/second-slider-icon-03.svg" alt="icon"></div>
                        <div class="second-slider__text">We screen candidates and handle the time-consuming work, so that you can focus on hiring those who suit your needs best</div>
                    </div>
                    </div>
                </div>
      
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import '../../assets/main.scss';
.second {
  position: relative;
  width: calc(100% - 30px);
  margin: -45px auto 0;

  @include min(769) {
    width: calc(100% - 60px);
    margin: -80px auto 0;
  }

  .container {
    display: flex;
    flex-direction: column;
    min-height: 720px;
    padding: 30px 30px 0 30px;

    @include min(769) {
      min-height: 800px;
      padding: 100px 40px 0 40px;
    }
    @include min(1200) {
      padding: 100px 80px 0 80px;
    }
  }
}

.second__inn {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  overflow: hidden;
  margin: auto;
  pointer-events: none;
  border-radius: 16px;
  background-image: url('../../img/bg-second-mob.jpg');
  background-repeat: no-repeat;
  background-position: 50% 0;
  background-size: cover;

  @include min(769) {
    background-image: url('../../img/bg-second.jpg');
    background-position: 50% 0;
  }

  &::before {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 70%;
    content: '';
    pointer-events: none;
    background-image: linear-gradient(180deg, rgba(8, 28, 34, 0) 0%, rgba(8, 28, 34, .75) 100%);
  }
}

.second__btn {
  position: absolute;
  z-index: 1;
  top: -10px;
  right: 0;

  @include min(769) {
    top: 10px;
    right: 10px;
  }
  @include min(1200) {
    top: 130px;
    right: 10px;
  }
}

.second__title {
  font-family: $font;
  font-weight: 500;
  font-style: normal;
  line-height: 1.1;
  max-width: 600px;
  margin-bottom: auto;
  user-select: none;
  color: $deep-green;

  @include responsive-font(44, 32);
}

.second-slider {
  position: relative;
  overflow: hidden;
  padding-bottom: 80px;
}

  .swiper-pagination {
    bottom: 30px;
    text-align: left;
  }

.second-slider__icon {
  margin-bottom: 50px
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

  .swiper-wrapper {
    transition-timing-function: linear;
  }

  .swiper-slide {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: auto !important;
    height: auto;
  }


</style>