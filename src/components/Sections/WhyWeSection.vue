<template>
    <section class="why-we">
        <div class="container">
            <div class="why-we__list">
                <article class="why-we__item">
                    <div class="why-we__icon"><img src="../../img/why-we-icon-01.svg" alt="icon"></div>
                    <h2 class="why-we__title"><span>we understand you</span> and your long-term needs</h2>
                    <p class="why-we__descr">Our attention to detail and superior customer service can assist you in building your team and take the stress out of finding the best local and nationwide talent for your business in a matter of seconds</p>
                </article>
                <article class="why-we__item">
                    <div class="why-we__icon"><img src="../../img/why-we-icon-02.svg" alt="icon"></div>
                    <h2 class="why-we__title">we provide <span>hight quality standarts</span> of work</h2>
                    <p class="why-we__descr">Nothing should stop you from unlocking you and your offices maximum potential. Staffeak is known for the highest standards of timeliness, professionalism, and respect</p>
                </article>
                <article class="why-we__item">
                    <div class="why-we__icon"><img src="../../img/why-we-icon-03.svg" alt="icon"></div>
                    <h2 class="why-we__title">we use only <span>proven methodologies</span></h2>
                    <p class="why-we__descr">Our proven recruitment and training methodologies enable us to offer cost-effective permanent and temporary staffing in the US that meets your business needs</p>
                </article>
                <article class="why-we__item">
                    <div class="why-we__slogan"><span>At Your Service</span><span>24 Hours a Day, 7 Days a Week</span></div>
                </article>
            </div>
        </div>
    </section>
</template>    

<style lang="scss" scoped>
@import '../../assets/main.scss';

.why-we {
  padding-bottom: 120px;

  @include min(769) {
    padding-bottom: 200px;
  }
}

.why-we__list {
  display: flex;
  flex-wrap: wrap;
}

.why-we__item {
  display: flex;
  flex-direction: column;
  width: 100%;

  @include min(769) {
    width: 50%;
  }
}

.why-we__item:nth-child(1) {
  padding: 0 0 50px 0;
  border-bottom: 1px solid #e7edf4;

  @include min(769) {
    padding: 0 40px 40px 0;
    border-right: 1px solid #e7edf4;
    border-bottom: 1px solid #e7edf4;
    border-radius: 0 0 32px 0;
  }

  .why-we__icon {
    max-width: 39px;

    @include min(769) {
      max-width: 50px;
    }
  }
}

.why-we__item:nth-child(2) {
  padding: 50px 0 50px;
  border-bottom: 1px solid #e7edf4;

  @include min(769) {
    padding: 0 0 40px 40px;
    border: none;
  }

  .why-we__icon {
    max-width: 62px;

    @include min(769) {
      max-width: 80px;
    }
  }
}

.why-we__item:nth-child(3) {
  padding: 50px 0 70px 0;

  @include min(769) {
    padding: 40px 40px 0 0;
  }

  .why-we__icon {
    max-width: 67px;

    @include min(769) {
      max-width: 77px;
    }
  }
}

.why-we__item:nth-child(4) {
  @include min(769) {
    padding: 40px 0 0 40px;
    border-top: 1px solid #e7edf4;
    border-left: 1px solid #e7edf4;
    border-radius: 32px 0 0 0;
  }
}

.why-we__icon {
  margin-bottom: 30px;

  img {
    display: block;
    width: 100%;
  }
}

.why-we__title {
  font-family: $font;
  font-weight: 500;
  font-style: normal;
  line-height: 1.2;
  max-width: 295px;
  margin-bottom: 20px;
  color: $neutral-grey;

  @include responsive-font(24, 22);
  @include min(1025) {
    margin-bottom: 60px;
  }
  @include min(1200) {
    margin-bottom: 110px;
  }

  span {
    color: $deep-green;
  }
}

.why-we__descr {
  font-family: $font;
  font-size: 16px;
  font-weight: 500;
  font-style: normal;
  line-height: 1.1;
  color: $neutral-grey;
}

.why-we__slogan {
  margin-top: auto;

  span {
    font-family: $font;
    font-weight: 500;
    font-style: normal;
    line-height: 29px;
    display: block;
    text-align: right;

    @include responsive-font(24, 20);

    &:first-child {
      color: $neutral-grey;
    }

    &:nth-child(2) {
      color: $main-green;
    }
  }
}

</style>
