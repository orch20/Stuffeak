<template>
    <button class="search-main__btn"><span>Search</span>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path d="M21.7101 20.2896L18.8801 17.4696C20.4143 15.5743 21.1627 13.1625 20.971 10.7316C20.7793 8.3007 19.6621 6.03604 17.8499 4.40458C16.0376 2.77313 13.6684 1.89929 11.2308 1.96324C8.79317 2.02719 6.47304 3.02407 4.7488 4.74831C3.02456 6.47255 2.02768 8.79268 1.96373 11.2303C1.89977 13.6679 2.77362 16.0371 4.40507 17.8494C6.03653 19.6617 8.30119 20.7788 10.7321 20.9705C13.163 21.1622 15.5748 20.4138 17.4701 18.8796L20.2901 21.7096C20.3831 21.8033 20.4937 21.8777 20.6155 21.9285C20.7374 21.9793 20.8681 22.0054 21.0001 22.0054C21.1321 22.0054 21.2628 21.9793 21.3847 21.9285C21.5065 21.8777 21.6171 21.8033 21.7101 21.7096C21.8038 21.6166 21.8782 21.506 21.929 21.3842C21.9798 21.2623 22.0059 21.1316 22.0059 20.9996C22.0059 20.8676 21.9798 20.7369 21.929 20.615C21.8782 20.4932 21.8038 20.3826 21.7101 20.2896ZM4.00009 11.4996C4.00009 10.0162 4.43996 8.56619 5.26407 7.33283C6.08818 6.09946 7.25952 5.13816 8.62997 4.57051C10.0004 4.00285 11.5084 3.85432 12.9633 4.14371C14.4181 4.4331 15.7545 5.14741 16.8034 6.1963C17.8523 7.2452 18.5666 8.58157 18.856 10.0364C19.1454 11.4913 18.9968 12.9993 18.4292 14.3697C17.8615 15.7402 16.9002 16.9115 15.6669 17.7356C14.4335 18.5597 12.9835 18.9996 11.5001 18.9996C9.51097 18.9996 7.60331 18.2094 6.19679 16.8029C4.79027 15.3964 4.00009 13.4887 4.00009 11.4996Z" fill="#014750"/>
        </svg>
    </button>
</template>

<style lang="scss" scoped>
@import '../../../assets/main.scss';
.search-main__btn {
  font-family: 'Inter', sans-serif;
  font-size: 16px;
  font-weight: 600;
  font-style: normal;
  line-height: 1;
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  height: 52px;
  padding: 6px 20px 6px 30px;
  cursor: pointer;
  user-select: none;
  white-space: nowrap;
  text-decoration: none;
  color: $deep-green;
  border: none;
  border-radius: 30px !important;
  background: $gradient;
  box-shadow: none;

  @include min(769) {
    height: 60px;
  }

  &:hover {
    svg {
      transform: translateY(-5px);
    }
  }

  svg {
    display: block;
    flex: none;
    fill: $deep-green;
    width: 24px;
    height: 24px;
    transition: $transition;
  }
}
</style>