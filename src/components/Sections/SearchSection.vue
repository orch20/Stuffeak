<template>
    <section>
        <div class="top">
            <div class="container">
                <h1 class="top__title">Over 
                    <span class="top__title-highlight">100,000</span> 
                    <span class="top__title-italic">different business</span>
                    <br>in USA are looking for temp staff everyday
                </h1>
                <div class="top__subtitle">Unlike traditional staffing agencies, we connect you directly with professional staff</div>
                <SearchForm />
                <LogoSlider />
            </div>
        </div>
    </section>
</template>

<script setup>
import LogoSlider from '../Elements/LogoSlider.vue';
import SearchForm from '../Elements/SearchForm.vue';
</script>

<style lang="scss" scoped>
@import '../../assets/main.scss';

.top {
  position: relative;
  background-color: $deep-green;

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
    opacity: 1;
    background-image: url('../../img/bg-top.svg');
    background-position: 50% 50%;
  }

  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    padding-top: 90px;
    padding-bottom: 200px;

    @include min(769) {
      padding-bottom: 230px;
    }
  }
}

.top__title {
  font-family: $font;
  font-weight: 500;
  font-style: normal;
  line-height: 1.1;
  margin-bottom: 20px;
  text-align: center;
  color: $neutral-white;
}

.top__title-highlight {
  color: $fresh-mint;
}

.top__title-italic {
  font-family: $font-bold;
  font-weight: 600;
  font-style: italic;

  @include responsive-font(50, 36);
}

.top__subtitle {
  font-family: $font;
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  margin-bottom: 40px;
  text-align: center;
  color: $light-grey;
}
</style>
