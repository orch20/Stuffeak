<template>
    <div class="index-text">
        <div class="container">
            <div class="index-text__title">
                Do you need to help your practice run smoothly, eliminating unwanted downtime? Find
                <a href="#" class="index-text__title-link active">Quality
                    staffing</a>
                with Staffeak. Unlike traditional staffing, we regularly fill jobs for different types of business – from
                office workers to medicine personal.
            </div>
            <div class="index-text__footer">
                <div class="index-text__footer-ava"><img src="../../img/ava-trio.png" alt="img"></div>
                <div class="index-text__footer-text">12,265 people already finded a work</div>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@import '../../assets/main.scss';
.index-text {
  .container {
    padding-top: 100px;
    padding-bottom: 90px;

    @include min(769) {
      padding-top: 120px;
      padding-bottom: 120px;
    }
  }
}

.index-text__title {
  font-family: $font;
  font-weight: 400;
  font-style: normal;
  line-height: 1.2;
  margin-bottom: 30px;
  color: $deep-green;

  @include responsive-font(44, 32);
}

.index-text__title-link {
  font-size: 16px;
  font-weight: 600;
  line-height: 1;
  display: inline-flex;
  overflow: hidden;
  align-items: center;
  width: 0;
  height: 42px;
  margin-right: -13px;
  padding: 0;
  transition: .5s;
  transform: translateY(-2px) scale(0);
  text-align: center;
  white-space: nowrap;
  color: $deep-green;
  border: 2px solid transparent;
  border-radius: 25px;
  background-image: url('../../img/arr-right.svg');
  background-repeat: no-repeat;
  background-position: 90% 50%;

  @include min(600) {
    transform: translateY(-9px) scale(0);
  }
  @include min(1200) {
    transform: translateY(-13px) scale(0);
  }

  &.active {
    width: 190px;
    margin-right: 0;
    padding-right: 45px;
    padding-left: 20px;
    transform: translateY(-2px) scale(1);
    border-color: #0ad582;

    @include min(600) {
      transform: translateY(-9px) scale(1);
    }
    @include min(1200) {
      transform: translateY(-13px) scale(1);
    }
  }
}

.index-text__footer {
  display: flex;
  align-items: center;
}

.index-text__footer-ava {
  flex: none;
  margin-right: 10px;

  img {
    display: block;
    max-width: 100%;
  }
}

.index-text__footer-text {
  font-family: $font;
  font-weight: 500;
  font-style: normal;
  line-height: 1.2;
  color: $neutral-grey;

  @include responsive-font(18, 12);
}
</style>