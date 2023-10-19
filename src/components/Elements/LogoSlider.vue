<template>
  <div class="logos-slider-wrap">
    <div class="logos-slider__title">They are trusted Staffeak:</div>
    <!--BEGIN logos-slider-->
    <div class="logos-wrap">
      <div class="logo"><img src="../../img/logos/logo-01.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-02.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-03.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-04.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-05.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-06.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-07.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-08.svg" alt=""> </div>
      <div class="logo"><img src="../../img/logos/logo-09.svg" alt=""> </div>
    </div>
    <!--END   logos-slider-->
  </div>
</template>

<style lang="scss" scoped>
@import '../../assets/main.scss';

.logos-slider-wrap {
  position: absolute;
  right: 0;
  bottom: 110px;
  left: 0;
  overflow: hidden;
  width: 100%;
  margin: auto;
}

.logos-slider__title {

  font-size: 16px;
  font-weight: 500;
  line-height: 1.1;
  margin-bottom: 24px;
  text-align: center;
  color: $light-grey;
}

.logos-wrap {
  margin: 0 auto;
  /* text-align: center; */
  display: flex;
  align-items: center;
  justify-content: center;
}

.logo {
  margin-right: 60px;
}
</style>