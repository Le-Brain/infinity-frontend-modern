<template>
  <div class="main">
    <div class="main__title">
      <img src="~assets/images/logo.svg" />

      <h2 class="main__text"><span class="main__text-color">Вас приветствует</span> INFINITY</h2>
    </div>

    <img src="~assets/images/main.svg" />

    <div class="main__log">
      <NuxtLink class="btn" height="40" color="#FFFFFF" outlined to="/login">Войти</NuxtLink>

      <NuxtLink class="btn" height="40" color="#C7493A" outlined to="/registration">Регистрация</NuxtLink>
    </div>

    <img src="~assets/images/line.svg" />
  </div>
</template>

<script lang="ts">
export default {
  name: 'MainPage',
}
</script>

<style lang="scss">
.main {
  display: flex;
  height: 100%;
  width: 100%;
  box-sizing: border-box;
  flex-direction: column;
  align-items: center;
  background-color: #000000;
}
.main__title {
  text-align: center;
}
.main__text {
  color: #c7493a;
  font-weight: 700;
  font-size: 64px;
  line-height: 96px;
}
.main__text-color {
  color: #e0c3c3;
}
.main__log {
  margin-bottom: 62px;
}
.btn {
  text-decoration: none;
  font-size: 24px;
  width: 200px;
  height: 40px;
}
.btn:last-child {
  margin-left: 38px;
}
</style>
