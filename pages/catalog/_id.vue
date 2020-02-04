<template>
  <v-container>
    <v-breadcrumbs large :items="items" class="pa-0 display-2">
      <template v-slot:divider>
        <v-icon large color="primary">mdi-chevron-right</v-icon>
      </template>
    </v-breadcrumbs>
    <v-row>
      <v-col cols="12" md="4">
        <v-row>
          <v-col cols="12">
            <v-img :aspect-ratio="1" class="grey lighten-2"></v-img>
          </v-col>
          <v-col cols="3"><v-img :aspect-ratio="1" class="grey lighten-2"></v-img></v-col>
          <v-col cols="3"><v-img :aspect-ratio="1" class="grey lighten-2"></v-img></v-col>
          <v-col cols="3"><v-img :aspect-ratio="1" class="grey lighten-2"></v-img></v-col>
          <v-col cols="3"><v-img :aspect-ratio="1" class="grey lighten-2"></v-img></v-col>
        </v-row>
      </v-col>
      <v-col cols="12" md="8">
        <v-row>
          <v-col>
            <v-card flat tile class="px-9 py-10">
              <h1 class="display-3 mb-5">iPhone X 256 GB Black 2019 model</h1>
              <span class="mt-6">Цена</span>
              <h2 class="display-2 font-weight-bold">100,000 тг.</h2>
              <v-card-actions class="px-0 py-6">
                <v-btn x-large depressed outlined color="primary" class="to-cart-button border-15 text-none px-7">В корзину</v-btn>
                <v-btn x-large depressed class="primary border-15 text-none ml-5 px-10">Купить</v-btn>
              </v-card-actions>
              <h3>Описание</h3>
              <p class="grey--text text--darken-2">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque quas obcaecati iure possimus culpa iste, nulla beatae porro provident non tempora aliquam eos repudiandae fugit eveniet, eius sequi explicabo perspiciatis debitis architecto voluptatem modi ullam numquam dolorem. Repellat quo, expedita odio officia atque saepe, aliquid sunt magni eius facere, laboriosam asperiores porro explicabo ex sit optio rerum? Mollitia dolorum commodi illum nemo fugit, nulla minima distinctio eligendi sapiente, neque officia?</p>
              <div class="d-flex">
                <span class="mr-3">Цвета</span>
                <span class="showcase-color grey lighten-4"></span>
                <span class="showcase-color grey darken-4"></span>
                <span class="showcase-color deep-orange accent-1"></span>
              </div>
              <span class="mr-5">Память</span>
              <span>64 / 128 / 256</span>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <h3>Похожие продукты</h3>
    <v-row>
      <div class="d-flex products">
        <v-col v-for="item in 8" :key="item.id" lg="3" md="4" sm="6">
          <v-card flat tile>
            <v-img height="220" class="grey lighten-2"></v-img>
            <div class="d-flex flex-column pa-5">
              <span class="title product-name font-weight-regular">iPhone X 256 GB Black 2019 model</span>
              <span class="d-flex align-center my-1 ml-n1">
                <v-rating
                  readonly
                  dense
                  length="5"
                  half-increments
                  value="4.5"
                  background-color="amber lighten-2"
                  color="amber"
                />
                <span class="ml-1">(15)</span>
              </span>
              <span class="title font-weight-bold">100,000 kzt</span>
            </div>
          </v-card>
        </v-col>
      </div>
    </v-row>
  </v-container>
</template>

<script>

export default {
  components: {
  },
  data () {
    return {
      items: [
        {
          text: 'Каталог',
          href: '/'
        },
        {
          text: 'iPhone X 256 GB Black 2019 model'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.to-cart-button{
  border-width: 2px;
}
.showcase-color {
  width: 1.5rem;
  height: 1.5rem;
  border-radius: 50%;
  margin-left: .7rem;
}
.products {
  overflow-x: scroll;
}
</style>
