
import WhatMakesUsDifSlider from '../Elements/WhatMakesUsDifSlider.vue';
<template>
    <section class="second">
        <div class="second__inn"></div>
            <div class="container">
            <h2 class="second__title">What makes us <span class="italic">different</span> from the others?</h2>
            <WhatMakesUsDifSlider />
            </div>
            
    </section>
</template>

<script setup>
import WhatMakesUsDifSlider from '../Elements/WhatMakesUsDifSlider.vue';
</script>

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

</style>