<template>
  <section class="banner">
    <agile class="banner__mask"
      :dots="false" :mobileFirst="true"
      :arrows="false" :speed="750"
      :timing="'linear'" :fade="true"
      :autoplay="true" :pauseOnHover="false">
      <div class="slide slide--1"></div>
    </agile>

    <div class="banner__participate">
      <div class="banner__streaming">
        <a href="https://www.youtube.com/watch?v=md9iNDdAmVo&feature=youtu.be" class="banner__btn" target="_blank"><span>{{$t('bannerBtnLeft')}}</span></a>
      </div>
      <div class="banner__streaming">
        <a href="https://www.youtube.com/watch?v=9RtSod8EXn4&feature=youtu.be" class="banner__btn" target="_blank"><span>{{$t('bannerBtnRight')}}</span></a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Banner'
}
</script>

<style scoped lang="scss">
$font-family: 'Open+Sans', Microsoft JhengHei, 'Lato', sans-serif, Helvetica, Arial;

.banner {
  width: 100%;
  background: #424242; /* Old browsers */
  background: -moz-linear-gradient(top, #424242 50%, #b6b6b6 100%); /* FF3.6-15 */
  background: -webkit-linear-gradient(top, #424242 50%,#b6b6b6 100%); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(to bottom, #424242 50%,#b6b6b6 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  padding: 5px 5px 5px 5px;
  &__mask:after {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 0;
    content: '';
    /* background: linear-gradient(to right top, rgba(132, 233, 167, 0.8), rgba(147, 210, 240, 0.7)); */
  }

  &__title {
    text-align: center;
    width: 100%;
    font-family: $font-family;
    font-size: 64px;
    color: #FFF;
    left: 50%;
    margin: 0;
    position: absolute;
    top: 195px;
    transform: translate(-50%, -50%);
  }

  &__date {
    text-align: center;
    opacity: 0.8;
    font-family: $font-family;
    font-size: 48px;
    color: #FFF;
    left: 50%;
    margin: 0;
    position: absolute;
    top: 289px;
    transform: translate(-50%, -50%);
  }

  &__participate {
    cursor: pointer;
    width: 450px;
    position: absolute;
    top: 480px;
    left: 50%;
    transform: translate(-50%, -50%);
    display: table;

    a {
      display: block;
      background: #50E3C2;
      box-shadow: 0 2px 4px 0 rgba(22,101,69,0.50);
      border-radius: 100px;
    }

    a:active {
      position: relative;
      top: 1px;
    }

    a:hover {
      background: #43C3A6;
      text-decoration: none;
    }

    span {
      display: block;
      line-height: 50px;
      text-align: center;
      font-family: $font-family;
      font-size: 16px;
      color: #FFF;
      letter-spacing: 2.22px;
    }
  }
  &__streaming {
    margin: 0 auto;
    display: inline-block;
    width: 180px;
    margin: 0px 15px;
    padding: 0px 3px;

    a {
      text-decoration: none;
    }
  }
}

.slide {
  margin: 0 auto;
  max-width: 1100px;
  background: {
    position: center;
    size: 75%;
    repeat: no-repeat;
  }
  height: 550px;
  &--1 {
    background-image: url(../assets/banner5.png);
  }
}

@media only screen and (max-width: 767px) {
  .slide {
    background: {
      size: 90%;
    }
  }

  .banner__title {
    width: 486px;
    top: 158px;
  }

  .banner__date {
    width: 486px;
    top: 315px;
  }

  .banner__participate {
    top: 480px;
  }

  .banner__streaming {
    display: block;
    margin: 0 auto;
    margin-bottom: 15px;
  }
}

@media only screen and (max-width: 575px) {
  .slide {
    background: {
      size: 95%;
    }
  }

  .banner__title {
    top: 230px;
    width: 274px;
    font-size: 40px;
  }

  .banner__date {
    top: 350px;
    width: 274px;
    font-size: 30px;
  }
  
  .banner__participate {
    top: 450px;
  }

  .banner__streaming {
    display: block;
    margin: 0 auto;
    margin-bottom: 15px;
  }
}
</style>
