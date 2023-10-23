<template>
    <div class="registr-sec__right">
        <h2 class="registr-sec__title">
            <span>Start registration now</span>and see what Staffeak can do for your
            business
        </h2>
        <div class="registr-sec__subtitle">
            We are looking forward to working with you. Join the Staffeak family
        </div>
        <button class="direct-btn registr-sec__btn">
            <span>Try now</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="15" height="12" viewBox="0 0 15 12" fill="none">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M8.65704 0.238643L13.898 5.42386C14.2196 5.74205 14.2196 6.25794 13.898 6.57614L8.65704 11.7614C8.33544 12.0795 7.81401 12.0795 7.4924 11.7614C7.17079 11.4432 7.17079 10.9273 7.4924 10.6091L9.59821 8.52565C10.2334 7.89725 9.78837 6.81478 8.89489 6.81478H0.953939C0.503949 6.81478 0.13916 6.44999 0.13916 6C0.13916 5.55001 0.503949 5.18522 0.953939 5.18522H8.89489C9.78837 5.18522 10.2334 4.10275 9.59821 3.47435L7.4924 1.39091C7.17079 1.07272 7.17079 0.556834 7.4924 0.238643C7.81401 -0.0795478 8.33544 -0.0795478 8.65704 0.238643Z" fill="#0AD582"/>
            </svg>
        </button>
        <div class="blockquote registr-sec__blockquote">
            <span
                >Consider us as your partner - our best interest lies in connecting you with
                the employee(s) you are looking for.</span
            >
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import '../../assets/main.scss';
.registr-sec__right {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding-top: 50px;
  padding-bottom: 65px;

  @include min(769) {
    width: 50%;
    padding-top: 100px;
    padding-bottom: 100px;
    padding-left: 30px;
  }
  @include min(1025) {
    padding-left: 0;
  }
}

.registr-sec__title {
  font-family: $font;
  font-size: 44px;
  font-weight: 500;
  font-style: normal;
  line-height: 1.2;
  margin-bottom: 20px;
  color: $dark-green;

  @include responsive-font(44, 32);

  span {
    display: block;
    background: linear-gradient(90deg, #0ad582 0%, #a2f2c0 100%);
    -webkit-background-clip: text;
    background-clip: text;

    -webkit-text-fill-color: transparent;
    text-fill-color: transparent;
  }
}

.registr-sec__subtitle {
  font-family: $font;
  font-size: 18px;
  font-weight: 500;
  font-style: normal;
  line-height: 22px;
  margin-bottom: 40px;
  color: $dark-green;
}

.registr-sec__btn {
  width: 100%;
  max-width: 188px;
  margin-bottom: 75px;
  position: static;

  svg {
    fill: $main-green;
  }
}

.registr-sec__blockquote {
  margin-top: auto;
}

.direct-btn {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 600;
  font-style: normal;
  position: sticky;
  z-index: 1;
  bottom: 0;
  right: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 50px;
  /* margin-top: -50px; */
  margin-right: 15px;
  margin-left: auto;
  padding: 16px 24px;
  cursor: pointer;
  user-select: none;
  transform: translateY(-15px);
  white-space: nowrap;
  text-decoration: none;
  color: $deep-green;
  border: none;
  border-radius: 30px !important;
  background: $gradient;
  box-shadow: 0 12px 48px rgba(8, 28, 34, .16);

  @include min(1025) {
    margin-right: 40px;
    transform: translateY(-40px);
  }

  &.active {
    &::before {
      position: absolute;
      top: 1px;
      left: 0;
      width: 13px;
      height: 13px;
      content: '';
      border: 1px solid #fff;
      border-radius: 50%;
      background-color: $fresh-mint;
    }
  }

  &:hover {
    svg {
      transform: translateX(5px);
    }
  }

  svg {
    display: block;
    flex: none;
    fill: $deep-green;
    width: 14px;
    height: 12px;
    margin-left: 10px;
    transition: $transition;
  }
}
</style>