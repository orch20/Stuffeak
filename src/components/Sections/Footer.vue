<template>
    <div class="footer">
        <div class="container">
            <div class="footer__left"><a class="footer__logo" href="/"><img src="../../img/footer-logo.svg" alt="logo"></a>
            <div class="footer__info">
                <div class="footer__text-slogan">At Your Service <span>24 Hours a Day, 7 Days a Week</span></div>
                <div class="footer__info-row">
                <div class="footer__copyright">© 2023 Staffeak. All rights reserved.</div><a class="footer__privacy" href="/">Privacy Policy &amp; Terms of use</a>
                </div>
            </div>
            </div>
            <div class="footer__socials"><a class="footer__social-link" href="#" target="_blank" rel="nofollow noopener noreferrer">
                <img src="../../img/inst.svg" alt="inst logo"></a><a class="footer__social-link" href="#" target="_blank" rel="nofollow noopener noreferrer">
                <img src="../../img/fb.svg" alt="fb logo"></a><a class="footer__social-link" href="#" target="_blank" rel="nofollow noopener noreferrer">
                <img src="../../img/youtube.svg" alt="youtube logo"></a><a class="footer__social-link" href="#" target="_blank" rel="nofollow noopener noreferrer">
                <img src="../../img/in.svg" alt="in logo"></a></div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import '../../assets/main.scss';
.footer {
  padding-top: 15px;
  padding-bottom: 15px;
  background-color: $deep-green;

  @include min(600) {
    padding-top: 40px;
    padding-bottom: 40px;
  }

  .container {
    display: flex;
    flex-direction: column;

    @include min(769) {
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
    }
  }
}

.footer__left {
  display: flex;
  flex-direction: column;

  @include min(600) {
    flex-direction: row;
    align-items: center;
    margin-bottom: 30px;
  }
  @include min(769) {
    margin-bottom: 0;
  }
}

.footer__logo {
  display: block;
  flex: none;
  margin-right: 30px;
  margin-bottom: 20px;

  @include min(600) {
    margin-bottom: 0;
  }
  @include min(1025) {
    margin-right: 125px;
  }

  img {
    display: block;
    width: 53px;
  }
}

.footer__text-slogan {
  font-family: $font;
  font-size: 18px;
  font-weight: 500;
  font-style: normal;
  line-height: 1.2;
  margin-bottom: 23px;
  color: $neutral-white;

  span {
    color: $fresh-mint;
  }
}

.footer__info-row {
  position: absolute;
  bottom: 0;
  left: 20px;
  display: flex;
  flex-direction: column;

  @include min(600) {
    position: static;
    flex-direction: row;
  }
}

.footer__copyright,
.footer__privacy {
  font-family: $font;
  font-size: 12px;
  font-weight: 500;
  font-style: normal;
  line-height: 15px;
  white-space: nowrap;
  color: rgba(231, 237, 244, .5);
}

.footer__privacy {
  margin-top: 10px;
  text-decoration: underline;

  @include min(600) {
    margin-top: 0;
    margin-left: 40px;
  }

  &:hover {
    text-decoration: none;
    color: rgba(231, 237, 244, .5);
  }
}

.footer__socials {
  display: flex;
  align-items: center;
  padding-bottom: 90px;

  @include min(600) {
    padding-bottom: 0;
  }
}

.footer__social-link {
  display: block;
  flex: none;
  margin-right: 30px;

  @include min(769) {
    margin-right: 0;
    margin-left: 30px;
  }

  svg {
    fill: #f2eff4;
    width: 16px;
    height: 16px;
  }
}

</style>