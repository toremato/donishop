<template>
  <v-container>
    <h1 class="display-2 font-weight-bold mb-7">Корзина</h1>
    <v-window v-model="page">
      <v-window-item v-for="n in 3" :key="n">
        <v-card v-for="i in 3" :key="i" flat tile class="mb-12 d-flex">
          <v-col cols="12" md="9" class="d-flex flex-column pa-7 ma-0">
            <h2 class="font-weight-regular mb-4">iPhone X 256GB black A2019 model</h2>
            <span class="font-weight-bold">Описание</span>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sunt odio libero tempore. Atque laborum veniam ratione sapiente numquam facere. Architecto accusantium praesentium unde iusto veritatis ex eligendi quasi, mollitia ab.</p>
            <v-spacer />
            <v-card-actions class="pa-0">
              <v-btn depressed outlined color="red darken-4" class="text-none px-5">Удалить</v-btn>
              <v-btn depressed color="primary" class="text-none px-5">Купить</v-btn>
            </v-card-actions>
          </v-col>
          <v-col cols="12" md="3" class="grey lighten-2">
            <v-img min-height="200" />
          </v-col>
        </v-card>
      </v-window-item>
    </v-window>
    <v-pagination
      v-model="page"
      :length="3"
    />
  </v-container>
</template>

<script>

export default {
  data () {
    return {
      page: 1
    }
  }
}
</script>
