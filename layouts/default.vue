<template>
  <v-app>
    <v-app-bar :clipped-left="clipped" fixed flat app>
      <nuxt-link to="/" class="font-weight-bold title">DoniShop</nuxt-link>
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
      <nuxt-link to="/profile" class="ml-5">
        Войти
        <v-icon color="primary" class="ml-2">fas fa-user-circle</v-icon>
      </nuxt-link>
    </v-app-bar>
    <v-content>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2020</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style lang="scss" scoped>
.theme--light.v-application {
  background: #f2f2f2;
}
a {
  text-decoration: none;
  color: black !important;
}
header {
  padding: 0 9rem;
}
.container--fluid {
  padding: 3rem 10rem;
}
</style>
