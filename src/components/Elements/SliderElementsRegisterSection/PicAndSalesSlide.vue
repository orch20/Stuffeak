<template>
    <div class="registr-sec__slide-body registr-sec__slide-body--02">
      <div class="registr-sec__circle" style="background-color: #0AD582;"><img src="../../../img/faces/face-07.jpg" alt="people"></div>
      <div class="registr-sec__slide-text">Sales</div>
    </div>
</template>

<style lang="scss" scoped>
@import '../../../assets/main.scss';
.registr-sec__slide-body {
  display: flex;
  align-items: center;
  width: 320px;
  padding: 5px;
  border-radius: 56px;
  background-color: #fff;

  @include min(769) {
    flex-direction: column;
    width: 150px;
    border-radius: 75px;
  }

  .registr-sec__circle {
    width: 102px;
    height: 102px;

    @include min(769) {
      width: 140px;
      height: 140px;
    }

    &:first-child {
      margin-bottom: 0;
    }
  }

  &--01 {
    background-image: linear-gradient(270deg, #a2f2c0 0%, rgba(162, 242, 192, .25) 100%);

    @include min(769) {
      background-image: linear-gradient(180deg, #a2f2c0 0%, rgba(162, 242, 192, .25) 100%);
    }
  }

  &--02 {
    background-image: linear-gradient(270deg, #0ad594 0%, rgba(162, 242, 192, .38) 100%);

    @include min(769) {
      background-image: linear-gradient(180deg, #0ad594 0%, rgba(162, 242, 192, .38) 100%);
    }
  }
}

.registr-sec__circle {
  display: flex;
  overflow: hidden;
  justify-content: center;
  align-items: center;
  flex: none;
  width: 112px;
  height: 112px;
  border-radius: 50%;

  @include min(769) {
    width: 150px;
    height: 150px;
  }

  &:first-child {
    @include min(769) {
      margin-bottom: 20px;
    }
  }

  img {
    display: block;
    width: 100%;
    height: 100%;

    object-fit: cover;
    object-position: center;
  }
}

.registr-sec__slide-text {
  width: 100%;
  text-align: center;

  @include min(769) {
    width: auto;
    height: 170px;
    transform: rotate(180deg);

    writing-mode: vertical-lr;
  }
}
</style>