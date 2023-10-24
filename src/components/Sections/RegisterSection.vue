<template>
    <section class="registr-sec">
        <div class="container">
            <RegisterSectionSliders />
            <RegisterSectionRigthSide />
        </div>
    </section>
</template>

<script setup>
import RegisterSectionRigthSide from '../Elements/RegisterSectionRigthSide.vue'
import RegisterSectionSliders from '../Elements/RegisterSectionSliders.vue'

</script>

<style lang="scss" scoped>
@import '../../assets/main.scss';

.registr-sec {
  position: relative;
  overflow: hidden;
  background-color: rgba(162, 242, 192, .15);

  &::before {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 100%;
    content: '';
    transition: $transition;
    pointer-events: none;
    opacity: .05;
    background-image: url('../../img/bg-top.svg');
    background-position: 50% 50%;
  }

  .container {
    display: flex;
    flex-direction: column-reverse;

    @include min(769) {
      flex-direction: row;
    }
  }
}


</style>