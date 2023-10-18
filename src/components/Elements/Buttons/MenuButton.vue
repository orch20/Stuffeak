<template>
    <button class="menu-btn menu-btn--white">
        <div class="menu-btn__icon">
            <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="4" height="4" rx="1"></rect>
            <rect y="8" width="4" height="4" rx="1"></rect>
            <rect x="8" width="4" height="4" rx="1"></rect>
            <rect x="8" y="8" width="4" height="4" rx="1"></rect>
            <rect class="menu-btn__icon-center" x="4" y="4" width="4" height="4" rx="1"></rect>
            </svg>
        </div>
        <div class="menu-btn__text">menu</div>
        </button>
</template>

<style lang="scss" scoped>
@import '../../../assets/main.scss';
.menu-btn {
  position: absolute;
  top: 0;
  right: 15px;
  display: inline-flex;
  align-items: center;
  height: 40px;
  padding: 10px 20px;
  cursor: pointer;
  user-select: none;
  transition: $transition;
  text-decoration: none;
  pointer-events: auto;
  border: none;
  border-radius: 20px !important;
  background-color: transparent;
  box-shadow: none;

  @include min(769) {
    right: 40px;
  }
  @include min(1025) {
    display: none;
  }

  &.open {
    background-color: $main-green;

    .menu-btn__icon {
      border-right: 1px solid $fresh-mint;
    }

    .menu-btn__icon svg,
    .menu-btn__icon-center {
      fill: $neutral-white;
    }

    .menu-btn__text {
      color: $neutral-white;
    }
  }
}

.menu-btn__icon {
  display: flex;
  justify-content: center;
  align-items: center;
  flex: none;
  height: 20px;
  padding-right: 16px;
  transition: $transition;

  svg {
    fill: $main-green;
    width: 12px;
    height: 12px;
    transition: $transition;
  }
}

.menu-btn__icon-center {
  fill: transparent;
}

.menu-btn__text {
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  font-weight: 600;
  line-height: 15px;
  padding-left: 16px;
  user-select: none;
  transition: $transition;
  white-space: nowrap;
  text-transform: uppercase;
}

.menu-btn--white {
  background-color: $neutral-white;

  .menu-btn__icon {
    border-right: 1px solid $light-grey;
  }

  .menu-btn__text {
    color: $deep-green;
  }
}

.menu-btn--dark {
  background-color: $deep-green;

  .menu-btn__icon {
    border-right: 1px solid rgba(162, 242, 192, .25);
  }

  .menu-btn__text {
    color: $neutral-white;
  }
}
</style>