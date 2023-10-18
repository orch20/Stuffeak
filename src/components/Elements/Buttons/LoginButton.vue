<template>
    <button class="header__login">
        <svg xmlns="http://www.w3.org/2000/svg" width="25" height="24" viewBox="0 0 25 24" fill="none">
            <path d="M12.125 11C14.606 11 16.625 8.981 16.625 6.5C16.625 4.019 14.606 2 12.125 2C9.644 2 7.625 4.019 7.625 6.5C7.625 8.981 9.644 11 12.125 11ZM12.125 4C13.504 4 14.625 5.121 14.625 6.5C14.625 7.879 13.504 9 12.125 9C10.747 9 9.625 7.879 9.625 6.5C9.625 5.121 10.747 4 12.125 4Z" fill="#F8F8FC"/>
            <path d="M21.8789 20.778C20.8388 16.198 16.8275 13 12.125 13C7.4216 13 3.41123 16.199 2.37213 20.778C2.25012 21.317 2.58715 21.853 3.1262 21.975C3.66325 22.095 4.2003 21.759 4.32231 21.221C5.15339 17.559 8.36169 15 12.125 15C15.8874 15 19.0967 17.559 19.9278 21.222C20.0328 21.686 20.4458 22 20.9019 22C20.9749 22 21.0489 21.992 21.1249 21.976C21.6629 21.853 22.001 21.317 21.8789 20.778Z" fill="#F8F8FC"/>
        </svg>
    </button>
    <div class="header__login-text">Login / Registration</div>
</template>

<style lang="scss" scoped>
@import '../../../assets/main.scss';
.header__login {
      svg {
        fill: $neutral-white;
      }
    }
.header__login {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 32px;
  margin: 0;
  padding: 0;
  cursor: pointer;
  user-select: none;
  border: none;
  background-color: transparent;
  box-shadow: none;

  @include min(1025) {
    width: 32px;
  }

  svg {
    flex: none;
    fill: $dark-green;
    width: 20px;
    height: 20px;
  }
}

.header__login-text {
  font-size: 16px;
  font-weight: 600;
  line-height: 1.1;
  padding-left: 23px;
  white-space: nowrap;
  color: $neutral-white;

  @include min(1025) {
    display: none;
  }
}

</style>
