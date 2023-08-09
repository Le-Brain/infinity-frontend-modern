<template>
  <div class="loginPage">
    <Promo />

    <div class="log__section">
      <img src="~assets/images/logo.svg" />

      <div class="login-form">
        <h2 class="log__title">Авторизация</h2>

        <v-form>
          <v-text-field
            v-model="email"
            :counter="10"
            label="Логин / Email"
            hint="Введите ваш логин или email"
            placeholder="Введите логин"
            required
            outlined
          ></v-text-field>

          <v-text-field v-model="password" label="Пароль" name="password" hint="Введите пароль" counter></v-text-field>

          <div class="log__options">
            <v-switch label="Запомнить меня" color="#C7493A"></v-switch>

            <v-btn class="btn" height="64" width="155" color="#C7493A" outlined> Войти </v-btn>
          </div>
        </v-form>

        <p class="log__footnote">
          Нет аккаунта Infinity?
          <NuxtLink style="color: #c7493a" to="/registration">Зарегистрировать аккаунт</NuxtLink>
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'LoginPage',
  data() {
    return {
      email: '',
      password: '',
      rules: {
        required: (value: any) => !!value || 'Required.',
        min: (v: string | any[]) => v.length >= 8 || 'Min 8 characters',
        emailMatch: () => `The email and password you entered don't match`,
      },
    }
  },
}
</script>

<style lang="scss">
.loginPage {
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: #000000;
  margin-top: 30px;
  color: #ffffff;
}

.log__section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 35px 0 0 200px;
}

.log__options {
  display: flex;
  align-items: baseline;
}

.log__options div {
  margin-right: 20px;
}

.login-form {
  max-width: 759px;
  max-height: 716px;
  background: #110f0f;
  border-bottom: 10px solid #c7493a;
  margin-top: 90px;
  padding: 50px 155px 80px 155px;
}

.log__title {
  text-align: center;
  font-size: 64px;
  color: #ffffff;
  margin-bottom: 45px;
}

.log__footnote {
  border-top: 1px solid rgba(255, 255, 255, 0.12);
  padding-top: 48px;
  margin-top: 40px;
}

.login-form p,
a {
  margin-bottom: 0;
  text-decoration: none;
}

.login-form .v-form {
  background-color: #110f0f;
  margin: auto;
  width: 448px;
}

.login-form .v-form > div:nth-child(-n + 2) {
  margin-bottom: 55px;
}

.v-input--switch.v-input--dense .v-input--switch__track {
  height: 21px;
  width: 60px;
  border-radius: 10px;
}

.v-application--is-ltr .v-input--switch.v-input--dense .v-input--selection-controls__ripple {
  left: -10.5px;
  top: -8.5px;
}

.v-input--switch.v-input--dense .v-input--switch__thumb {
  width: 21px;
  height: 21px;
}

.v-input--switch__track {
  top: calc(50% - 10px);
}

.v-application--is-ltr .v-input--switch.v-input--is-dirty .v-input--selection-controls__ripple,
.v-application--is-ltr .v-input--switch.v-input--is-dirty .v-input--switch__thumb {
  transform: translate(45px, 0);
}

.v-input--switch .v-input--selection-controls__input {
  width: 64px;
  margin-right: 12px;
}

.log__options .v-label {
  font-size: 22px;
}

.log__options .v-btn__content {
  font-size: 24px;
}
</style>
