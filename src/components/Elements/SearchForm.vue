<template>
    <form class="search-main">
        <div class="search-main__select">
            <select>
                <option value="" disabled selected hidden>State</option>
                <option v-for="state in states" :key="state" value="{{state}}">{{ state }}</option>
             </select>
            </div>
            <div class="search-main__select">
            <select>
                <option value="" disabled selected hidden>Industry</option>
                <option v-for="industry in industries" :key="industry" value="{{industry}}">{{ industry }}</option>
            </select>
            </div>
            <div class="search-main__select">
            <select>
                <option value="" disabled selected hidden>Specialty</option>
                <option v-for="specialty in specialties" :key="specialty" value="{{speciality}}">{{ specialty }}</option>
            </select>
        </div>
        <SearchMainButton/>
    </form>
</template>

<script setup>
import SearchMainButton from './Buttons/SearchMainButton.vue';

// -----------------------------------------   TEMPORARY DATA   -----------------------------------------
const states = ["Alabama","Nebraska","Virginia","New Hampshire", "Massachusetts","Rhode Island", "Connecticut", "Vermont", "Maine", "New York", "New Jersey", "Pennsylvania", "Delaware", "Maryland", "North Carolina", "South Carolina", "Utah"];
const industries = ["Industry-01", "Industry-02", "Industry-03"];
const specialties = ["Specialty-01", "Specialty-02", "Specialty-03"];
// ------------------------------------------------------------------------------------------------------

</script>

<style lang="scss" scoped>
@import '../../assets/main.scss';
.search-main {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 500px;
  margin-bottom: 30px;
  padding: 1px;
  border-radius: 32px;
  background-color: transparent;

  @include min(769) {
    overflow: hidden;
    flex-direction: row;
    max-width: 820px;
    border: 1px solid $light-grey;
    background-color: #fff;
  }
}

.search-main__select,
.search-main__btn {
  width: 100%;

  @include min(769) {
    width: 25%;
  }
}

.search-main__select {
  position: relative;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  height: 54px;
  margin-bottom: 10px;
  border: 1px solid $light-grey;
  border-radius: 28px;
  background-color: $neutral-white;

  @include min(769) {
    overflow: visible;
    height: 60px;
    margin-bottom: 0;
    border: none;
    background-color: transparent;
  }

  &:first-child {
    &::before {
      display: none;
    }
  }

  &::before {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    width: 1px;
    height: 36px;
    margin: auto;
    content: '';
    background-color: $light-grey;
  }

  &::after {
    position: absolute;
    top: 0;
    right: 24px;
    bottom: 0;
    height: 8px;
    margin: auto;
    content: '';
    pointer-events: none;
    border-top: 6px solid $neutral-grey;
    border-right: 4px solid transparent;
    border-left: 4px solid transparent;
  }

  select {
    line-height: 1;
    overflow: hidden;
    width: 100%;
    height: 100%;
    padding-right: 30px;
    padding-left: 20px;
    text-overflow: ellipsis;
    color: $neutral-grey;
    border: none;

    -webkit-appearance: none;
    -moz-appearance: none;
  }

  select::-ms-expand {
    display: none;
  }

}
</style>