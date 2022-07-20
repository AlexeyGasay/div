<template>
  <div class="global_nav">
    <div class="global_nav__burger">
      <img
        src="../assets/banner/Menu.png"
        alt="Menu"
      >
    </div>

    <div class="navigation_info">
      <div class="navigation_info__decor_item"></div>
      <div class="navigation_info__decor_item"></div>

      <div class="navigation_info__current_page">
        <span class="navigation_info__current_page_num">03</span>
        <span class="navigation_info__current_page_name">Подсказки</span>
      </div>

      <div class="navigation_info__decor_item"></div>
    </div>

    <div class="global_nav__scroll_down">
      <p class="scroll_down__text">Скрольте вниз</p>

      <img
        src="../assets/banner/scroll-down.svg"
        alt="scroll"
      >
    </div>

  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.global_nav {
  position: fixed;
  left: 0;
  top: 0;
  padding: 40px 0 0 35px;
  height: 100vh;
}

.global_nav__burger {
  cursor: pointer;
}

.navigation_info {
  position: absolute;
  top: 15%;
}

.navigation_info__decor_item {
  width: 10px;
  height: 2px;
  background: #333;
  margin: 50px 0;
}

.navigation_info__current_page {
  display: flex;
  align-items: center;
  color: #333;
  padding-bottom: 5px;
  border-bottom: 1px solid #333;
}

.navigation_info__current_page_num {
  margin-right: 20px;
  font-size: 16px;
  font-family: "Kinopoisk-semibold", sans-serif;
}

.navigation_info__current_page_name {
  font-size: 14px;
  font-family: "Kinopoisk-regular";
}

// SCROLL DOWN
.global_nav__scroll_down {
  display: flex;
  flex-direction: column;
  position: absolute;
  bottom: 27px;

  img {
    align-self: center;
  }
}

.scroll_down__text {
  font-size: 14px;
  color: #333333;
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  margin-bottom: 25px;
  font-family: "Kinopoisk-regular";
}

.site_name {
  position: absolute;
  right: 0;
}
</style>