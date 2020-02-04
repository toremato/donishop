<template>
  <div id="login-main">
    <div class="gradient-bg"></div>
    <div class="triangle"></div>
    <v-container class="login-content mb-12">
      <h1 class="white--text my-7">Добро пожаловать</h1>
      <div class="d-flex">
        <v-form class="registration-form white border-20">
          <h2 class="mb-4">Регистрация</h2>
          <label for="name">Имя Фамилия</label>
          <v-text-field
            id="name"
            placeholder="Franz Kafka"
            solo
            hide-details
            full-width
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <label>Номер телефона</label>
          <v-text-field
            placeholder="+7 777 000 00 00"
            solo
            full-width
            hide-details
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <label>Электронный адрес</label>
          <v-text-field
            placeholder="example@gmail.com"
            solo
            full-width
            hide-details
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <label>Придумайте пароль</label>
          <v-text-field
            placeholder="* * * * *"
            solo
            full-width
            hide-details
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <label>Повторите пароль</label>
          <v-text-field
            placeholder="* * * * *"
            solo
            full-width
            hide-details
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <v-btn outlined large block color="primary" class="register-btn mt-8 text-none font-weight-bold">Регистрация</v-btn>
        </v-form>
        <v-form class="login-form align-self-center mx-auto">
          <h2 class="mb-4">Авторизация</h2>
          <label>Номер телефона</label>
          <v-text-field
            placeholder="+7 777 000 00 00"
            solo
            full-width
            hide-details
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <label>Пароль</label>
          <v-text-field
            placeholder="* * * * *"
            solo
            full-width
            hide-details
            flat
            dense
            single-line
            class="border-10 mb-4"
          />
          <v-btn block large class="mt-6 mb-2 primary text-none">Войти</v-btn>
          <a href="">Забыли пароль?</a>
        </v-form>
      </div>
    </v-container>
  </div>
</template>

<script>

export default {
}
</script>

<style lang="scss" scoped>
#login-main {
  z-index: 1;
  position: relative;
}
.gradient-bg {
  z-index: -1;
  height: 250px;
  width: 100%;
  position: absolute;
  background: rgb(135,103,242);
  background: linear-gradient(90deg, rgba(135,103,242,1) 50%, rgba(50,54,116,1) 100%);
}
.triangle {
  width: 0;
  height: 0;
  z-index: -1;
  position: absolute;
  top: 180px;
  border-style: solid;
  border-width: 0 0 70px 100vw;
  border-color: transparent transparent #f2f2f2 transparent;
}
.login-content {
  // position: absolute;
  // z-index: -10;
  // background: yellow;
}
.registration-form {
  padding: 2rem 4rem;
  width: 38rem;
}
.login-form {
  width: 20rem;
}
.register-btn {
  color: black;
  border: 2px solid #8968f6;
}
</style>

<style lang="scss">
.registration-form .v-text-field--solo > .v-input__control > .v-input__slot {
  background: rgba(200, 200, 200,.24) !important;
}
</style>
