<template>
    <nav class="menu">
        <ul class="menu__list">
        <li class="menu__item"><a href="#" class="menu__link">About</a></li>
        <li class="menu__item"><a href="#" class="menu__link">How it works</a></li>
        <li class="menu__item"><a href="#" class="menu__link">Pricing</a></li>
        <li class="menu__item"><a href="#" class="menu__link">Our sponsors</a></li>
        <li class="menu__item"><a href="#" class="menu__link">Contact</a></li>
        </ul>
    </nav>
</template>

<style lang="scss">
@import '../assets/main.scss';

.menu {
  margin-top: auto;
  transition: opacity $transition;
  pointer-events: none;
  opacity: 0;

  @include min(1025) {
    margin-top: 0;
    pointer-events: auto;
    opacity: 1;
  }
}

.menu--co {
  transition: opacity $transition;
  pointer-events: none;
  opacity: 0;

  @include min(1025) {
    margin-left: auto;
    pointer-events: auto;
    opacity: 1;
  }
}

.menu__list {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin: 0 0 40px 0;
  padding: 0;
  list-style: none;

  @include min(600) {
    margin: 0 0 95px 0;
  }
  @include min(1025) {
    flex-direction: row;
    margin-bottom: 0;
  }
}

.menu__item {
  position: relative;
  margin-bottom: 27px;

  @include min(1025) {
    margin-bottom: 0;
    padding: 0 14px;
  }

  &:last-child {
    margin-bottom: 0;
  }
}

.menu__link {
  font-size: 32px;
  font-weight: 500;
  line-height: 1.1;
  user-select: none;
  white-space: nowrap;
  text-decoration: none;
  color: $dark-green;

  @include min(1025) {
    font-size: 12px;
    line-height: 15px;
    position: relative;
    display: block;
    text-transform: uppercase;
  }

  &::before {
    @include min(1025) {
      position: absolute;
      right: 0;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 1px;
      margin: auto;
      content: '';
      transition: $transition;
      transform: scale(0);
      background-color: $dark-green;
    }
  }

  &:hover {
    &::before {
      transform: scale(1);
    }
  }

  & + span {
    font-size: 9px;
    font-weight: 600;
    line-height: 1;
    position: absolute;
    top: 0;
    right: -8px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 16px;
    height: 16px;
    text-align: center;
    color: $deep-green;
    border-radius: 50%;
    background-color: $main-green;

    @include min(1025) {
      top: -10px;
      right: 2px;
    }
  }
}

</style>