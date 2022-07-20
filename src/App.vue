<template>
  <div class="template">
    <GlobalNav />
    <BannerComp />

    <div class="template__site_name">
      <p class="site_name__text">hd.kinopoisk.ru</p>
    </div>

  </div>
</template>

<script>
import BannerComp from "./components/BannerComp.vue";
import GlobalNav from "./components/GlobalNav.vue";

export default {
  name: "App",
  components: {
    BannerComp,
    GlobalNav,
  },
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  text-decoration: none;
}

.template {
  position: relative;
}

.template__site_name {
  right: 0;
  top: 38%;
  position: fixed;
  padding-right: 30px;
}

.site_name__text {
  font-family: "Kinopoisk-lite";
  font-size: 14px;
  writing-mode: vertical-lr;
}

/* ШРИФТЫ */

@font-face {
  font-family: "Futura-bold";
  src: url("./assets/fonts/futura-bold.woff2");
}
@font-face {
  font-family: "Kinopoisk-regular";
  src: url("./assets/fonts/kinopoisk-regular.woff2");
}
@font-face {
  font-family: "Kinopoisk-bold";
  src: url("./assets/fonts/kinopoisk-bold.woff2");
}
@font-face {
  font-family: "Kinopoisk-semibold";
  src: url("./assets/fonts/kinopoisk-semibold.woff2");
}
@font-face {
  font-family: "Kinopoisk-light";
  src: url("./assets/fonts/kinopoisk-light.woff2");
}
@font-face {
  font-family: "Kinopoisk-lite";
  src: url("./assets/fonts/kinopoisk-lite.woff2");
}
</style>
