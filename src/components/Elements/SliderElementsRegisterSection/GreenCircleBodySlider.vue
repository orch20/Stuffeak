<template>
    <div class="registr-sec__circle" style="background-color: #0AD582;"></div>
    <div class="registr-sec__circle" style="background-color: #0AD582;"></div>
</template>

<style lang="scss" scoped>
@import '../../../assets/main.scss';

.registr-sec__circle {
  
  flex: none;
  width: 112px;
  height: 112px;
  border-radius: 50%;

  @include min(769) {
    width: 150px;
    height: 150px;
  }

 

  
}

</style>        