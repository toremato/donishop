<template>
  <v-app>
    <v-app-bar flat app class="app-bar">
      <v-container>
        <v-toolbar flat class="p-0">
          <nuxt-link to="/" class="font-weight-bold headline">DoniShop</nuxt-link>
          <v-spacer />
          <nuxt-link to="/" class="ml-5">
            Главная
            <v-icon color="primary" class="ml-2">fas fa-home</v-icon>
          </nuxt-link>
          <nuxt-link to="/cart" class="ml-5">
            Корзина
            <v-icon color="primary" class="ml-2">fas fa-shopping-basket</v-icon>
          </nuxt-link>
          <nuxt-link to="/orders" class="ml-5">
            Мои заказы
            <v-icon color="primary" class="ml-2">fas fa-shopping-bag</v-icon>
          </nuxt-link>
          <nuxt-link to="/login" class="ml-5">
            Tore
            <v-icon color="primary" class="ml-2">fas fa-user-circle</v-icon>
          </nuxt-link>
        </v-toolbar>
      </v-container>
    </v-app-bar>
    <v-content>
      <v-container fluid class="pa-0 ma-0">
        <nuxt />
      </v-container>
    </v-content>
    <v-footer class="grey darken-4">
      <!-- <span>&copy; 2020</span> -->
      <v-container>
        <v-row>
          <v-col
            v-for="n in 4"
            :key="n"
            cols="12"
            md="3"
            sm="6"
            class="white--text d-flex flex-column"
          >
            <h4 class="primary--text title">Lorem ipsum</h4>
            <span>Lorem ipsum</span>
            <span>Lorem ipsum</span>
            <span>Lorem ipsum</span>
            <span>Lorem ipsum</span>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.theme--light.v-application {
  background: #f2f2f2;
  // background: transparent;
  // z-index: -2;
}
a {
  text-decoration: none;
  color: black !important; // TODO get rid of this
}
header {
  // padding: 0 9rem;
}
.container--fluid {
  // padding: 3rem 10rem;
}
.v-footer {
  // background: black;
}
</style>
<style lang="scss">
.app-bar .v-toolbar__content {
  padding: 0;
}
</style>
