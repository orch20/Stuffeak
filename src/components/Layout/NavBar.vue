<template>
    <header class="header header--transparent">
      <div class="container">
        <LogoStuffeak />
        <NavMenu />
        <div class="header__right">
          <LoginButton />
          <PartnerButton />
        </div>
        <MenuButton />
      </div>
    </header> 
</template>

<script setup>
  import LogoStuffeak from '../LogoStuffeak.vue'
import NavMenu from '../NavMenu.vue'
import LoginButton from '../Elements/Buttons/LoginButton.vue'
import PartnerButton from '../Elements/Buttons/PartnerButton.vue'
import MenuButton from '../Elements/Buttons/MenuButton.vue'
</script>

<style lang="scss">
@import '../../assets/main.scss';

.header {
  position: absolute;
  z-index: 100;
  top: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  padding: 17px 0;
  transition: $transition;
  pointer-events: none;
  background-color: transparent;

  @include min(1025) {
    height: auto ;
  }

  &::before {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    margin: auto;
    content: '';
    transition: $transition;
    pointer-events: none;
    opacity: 0;
    background-image: url('../../img/bg-top.svg');
    background-position: 50% 50%;
  }

  .container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    height: 100%;

    @include min(1025) {
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      height: auto;
    }
  }

  &.open {
    position: fixed;
    background-color: $dark-green;
    .container {
      padding-bottom: 60px;
      @include min(1025) {
        padding-bottom: 0;
      }
    }

    &::before {
      opacity: .3;
    }

    .logo__text {
      fill: $neutral-white;
    }

    .menu,
    .menu--co {
      transition: .5s .4s;
      pointer-events: auto;
      opacity: 1;
    }

    .menu__link {
      color: $neutral-white;
    }

    .header__right {
      transition: .5s .8s;
      pointer-events: auto;
      opacity: 1;
    }

    .header__settings {
      transition: .5s .8s;
      pointer-events: auto;
      opacity: 1;
    }
  }
}

.header__right {
  display: flex;
  flex-direction: column-reverse;
  align-items: flex-start;
  //padding-bottom: 60px;
  transition: opacity .5s;
  pointer-events: none;
  opacity: 0;

  @include min(600) {
    //padding-bottom: 20px;
  }
  @include min(1025) {
    flex-direction: row;
    align-items: center;
    //padding-bottom: 0;
    pointer-events: auto;
    opacity: 1;
  }
}

.header__settings {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  transition: opacity $transition;
  pointer-events: none;
  opacity: 0;

  @include min(1025) {
    display: none;
  }
}

.header__settings-menu {
  margin: 0 0 27px 0;
  padding: 0;
  list-style: none;
}

.header__settings-item {
  margin-bottom: 10px;

  &:last-child {
    margin-bottom: 0;
  }
}

.header__settings-link {
  font-size: 18px;
  font-weight: 500;
  line-height: 1.2;
  color: $neutral-white;
}

/* begin HALF */
.header--half {
  .container {
    max-width: 100%;

    @include min(769) {
      padding-right: 40px;
      padding-left: 40px;
    }
  }

  .menu {
    @include min(1025) {
      margin-left: auto;
    }
  }

  .header__right {
    @include min(1025) {
      justify-content: flex-end;
      width: calc(50% + 25px);
    }
  }
}

/* end   HALF */

//-------------------------------------------
.header--transparent {
  .logo__text {
    fill: $neutral-white;
  }

  .menu__link {
    color: $neutral-white;

    &::before {
      background-color: $neutral-white;
    }
  }

  .header__login {
    svg {
      fill: $neutral-white;
    }
  }

  
}
</style>