<template>
  <div class="banner">
    <nav class="banner__nav">

      <a href="#">
        <img
          class="banner__logo"
          src="../assets/banner/logo.png"
          alt="logo"
        >
      </a>

    </nav>

    <div class="banner__slider_container">
      <h2 class="slider_container__header">ОНИ ДОЛЖНЫ ЧТО-ТО ЗНАТЬ</h2>

      <div class="slider__progress_bar">
        {{currendtSlide+1 + "/" + (sliderData.length)}}
      </div>

      <div class="slider_track">

        <transition-group name="slider-handler">

          <img
            class="slider_track__handler slider_track__handler--left"
            v-show="currendtSlide > 0"
            :key="1"
            @click="sliderHandler('prev')"
            src="../assets/banner/slider-left-arrow.svg"
            alt=""
          >
        </transition-group>

        <div class="slider_track__change_content">

          <img
            class="change_content__cover"
            src="../assets/banner/change-content-cover.png"
            alt=""
          >

          <div class="change_content__image_box">
            <img
              src="../assets/banner/slider-img1.png"
              alt=""
            >
          </div>

          <p class="change_content__text">
            {{sliderData[currendtSlide].text}}
          </p>

        </div>

        <transition-group name="slider-handler">

          <img
            class="slider_track__handler slider_track__handler--right"
            v-show="currendtSlide < sliderData.length - 1"
            :key="2"
            @click="sliderHandler('next')"
            src="../assets/banner/slider-right-arrow.svg"
            alt=""
          >

        </transition-group>

      </div>

      <div class="slider__search_promo">

        <a
          class="search_promo__link"
          href="#"
        >
          Искать промокод

          <img
            class="search_promo__image"
            src="../assets/banner/promo-arrow.svg"
            alt="promo-arrow"
          >
        </a>

      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: "BannerComp",
  props: {},

  data() {
    return {
      currendtSlide: 0,
      sliderData: [
        {
          id: 1,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для первого примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 2,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для второго примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 3,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для третьего примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 4,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для четвертого примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 5,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для пятого примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 6,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для шестого примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 7,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для седьмого примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
        {
          id: 8,
          image:
            "https://sun9-60.userapi.com/impf/E9oB_NERSEdKmyahd-9oDE5EDu_h8mTlRKRzfQ/BM8bbcoEy_s.jpg?size=304x436&quality=95&sign=cb362507862b7aac590b80ea538a0f3a&type=album",
          text: `Для восьмого примера мы показали вам его лицо. В первой серии он прячется в подвале
              за мониторами, и пусть борода не собьёт вас с толку. Найдите героя и нажмите на паузу —
              ему не терпится отдать вам промокод.`,
        },
      ],
    };
  },

  methods: {
    sliderHandler(direction) {
      let dataLength = this.sliderData.length;

      if ((direction == "next") & (this.currendtSlide + 1 < dataLength)) {
        this.currendtSlide += 1;
      } else if ((direction == "prev") & (this.currendtSlide >= 1)) {
        this.currendtSlide -= 1;
      }
    },
  },
};
</script>

<style scoped lang="scss">
.banner {
  background-image: url("../assets/banner/banner-bg.png");
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
  overflow: hidden;
}

.banner__nav {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 25px;
}

// SLIDER
.banner__slider_container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.slider_container__header {
  margin-top: 25px;
  font-family: "Futura-bold", sans-serif;
  font-size: 45px;
  line-height: 72px;
  color: #ffcc64;
}

.slider__progress_bar {
  margin-top: 35px;
  font-size: 15px;
  background: #fff;
  padding: 17px;
  border-radius: 100%;
  font-family: "Kinopoisk-bold", sans-serif;
}

.slider_track {
  display: flex;
  align-items: center;
  margin: 50px 30px 0 30px;
  padding: 0 10px;
}

// SLIDER HANDLERS

.slider_track__handler {
  cursor: pointer;
  position: relative;
  z-index: 30;
  transition: 0.3s;
}

.slider_track__handler--left {
  left: 30px;
}
.slider_track__handler--right {
  right: 30px;
}

@keyframes slider_handler_enter {
  0% {
    opacity: 0;
    transform: scale(0);
  }

  100% {
    opacity: 1;
    transform: scale(1);
  }
}
@keyframes slider_handler_leave {
  0% {
    opacity: 1;
    transform: scale(1);
  }

  100% {
    opacity: 0;
    transform: scale(0);
  }
}

.slider-handler-enter-active {
  animation: slider_handler_enter 0.3s;
}
.slider-handler-leave-active {
  animation: slider_handler_leave 0.3s;
}
// CHANGE CONTENT
.slider_track__change_content {
  position: relative;
  z-index: 20;
  overflow: hidden;
  text-align: center;
}

.change_content__cover {
  position: absolute;
  z-index: 10;
  top: 100px;
  left: 200px;
  right: 0;
  margin: auto;
}

.change_content__image_box {
  z-index: 5;
  left: 0;
  right: 0;
  margin: auto;
  position: relative;
  min-height: 200px;
  overflow: hidden;

  img {
    top: 0;
    left: 0;
    right: 0;
    margin: auto;
    z-index: 20;
    position: absolute;
    max-width: 303px;
  }
}

.change_content__text {
  position: relative;
  z-index: 10;
  font-size: 20px;
  line-height: 32px;
  text-align: center;
  max-width: 902px;
  font-family: "Kinopoisk-light", sans-serif;
  letter-spacing: 0.4px;
  transition: 0.3s;
}

// PROMO

.slider__search_promo {
  position: relative;
  z-index: 20;
  margin-top: 20px;
}

.search_promo__link {
  font-family: "Kinopoisk-light";
  color: #333333;
  display: flex;
  align-items: center;
  padding: 15px;
}

.search_promo__image {
  margin-left: 15px;
}
</style>
