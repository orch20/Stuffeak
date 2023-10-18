<template>
    <button class="btn-with-icon header__partner-btn popup-open">Become a partner
        <svg xmlns="http://www.w3.org/2000/svg" width="15" height="12" viewBox="0 0 15 12" fill="none">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M8.65704 0.238643L13.898 5.42386C14.2196 5.74205 14.2196 6.25794 13.898 6.57614L8.65704 11.7614C8.33544 12.0795 7.81401 12.0795 7.4924 11.7614C7.17079 11.4432 7.17079 10.9273 7.4924 10.6091L9.59821 8.52565C10.2334 7.89725 9.78837 6.81478 8.89489 6.81478H0.953939C0.503949 6.81478 0.13916 6.44999 0.13916 6C0.13916 5.55001 0.503949 5.18522 0.953939 5.18522H8.89489C9.78837 5.18522 10.2334 4.10275 9.59821 3.47435L7.4924 1.39091C7.17079 1.07272 7.17079 0.556834 7.4924 0.238643C7.81401 -0.0795478 8.33544 -0.0795478 8.65704 0.238643Z" fill="#0AD582"/>
    </svg>
    </button>
</template>

<style lang="scss" scoped>
@import '../../../assets/main.scss';
.btn-with-icon {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 600;
  line-height: 1;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  height: 46px;
  padding: 6px 24px;
  cursor: pointer;
  user-select: none;
  white-space: nowrap;
  text-decoration: none;
  color: $neutral-white;
  border-width: 2px;
  border-style: solid;
  border-color: $light-grey;
  border-radius: 25px !important;
  background-color: transparent;
  box-shadow: none;

  &:hover {
    svg {
      transform: translateX(5px);
    }
  }

  svg {
    display: block;
    flex: none;
    fill: $main-green;
    width: 14px;
    height: 14px;
    margin-left: 10px;
    transition: $transition;
  }
}

.header__partner-btn {
      color: $neutral-white;
      border-color: $light-grey;
    }
.header__partner-btn {
  margin-bottom: 35px;
  /* color: $dark-green;
  border-color: $dark-green; */

  @include min(1025) {
    margin-bottom: 0;
    margin-left: 10px;
  }
  @include min(1200) {
    margin-left: 30px;
  }
}

</style>