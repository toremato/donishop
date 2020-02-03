<template>
  <v-container class="main-wrapper">
    <h1 class="display-2 font-weight-bold mb-7">Поиск</h1>
    <v-row no-gutters class="d-flex align-center">
      <!-- <v-col> -->
      <v-text-field solo flat hide-details class="main-search" placeholder="Что вы искали?" />
      <!-- </v-col> -->
      <!-- <v-col cols="3"> -->
        <!-- <div> -->
      <v-btn tile depressed large height="48" class="deep-purple darken-2 deep-purple--text text--lighten-3 text-none px-7">Фильтр</v-btn>
      <v-btn tile depressed large height="48" class="search-btn primary text-none px-10">Поиск</v-btn>
        <!-- </div> -->
      <!-- </v-col> -->
    </v-row>
    <v-card flat outlined class="d-flex flex-wrap pa-5 mt-7 filters">
      <div class="my-2 mx-5">
        <span>Выберите категорию</span>
        <v-select
          :menu-props="{ offsetY: true }"
          filled
          dense
          solo
          flat
          hide-details
        />
      </div>
      <div class="my-2 mx-5">
        <span>Укажите цену</span>
        <v-select
          :menu-props="{ offsetY: true }"
          filled
          dense
          solo
          flat
          hide-details
        />
      </div>
      <div class="my-2 mx-5">
        <span>Компания</span>
        <v-select
          :menu-props="{ offsetY: true }"
          filled
          dense
          solo
          flat
          hide-details
        />
      </div>
      <div class="my-2 mx-5">
        <span>Память</span>
        <v-select
          :menu-props="{ offsetY: true }"
          filled
          dense
          solo
          flat
          hide-details
        />
      </div>
      <div class="my-2 mx-5">
        <span>Цвет</span>
        <v-select
          :menu-props="{ offsetY: true }"
          filled
          dense
          solo
          flat
          hide-details
        />
      </div>
      <div class="my-2 mx-5">
        <span>Сортировать по</span>
        <v-select
          :menu-props="{ offsetY: true }"
          filled
          dense
          solo
          flat
          hide-details
        />
      </div>
    </v-card>
    <h2 class="mt-7 font-weight-bold">Результат поиска</h2>
    <h4 class="font-weight-light">Всего результатов: 10</h4>
    <v-row>
      <v-col v-for="item in searchResults" :key="item.id" lg="3" md="4" sm="6">
        <v-card flat tile>
          <v-img height="220" class="grey lighten-2"></v-img>
          <div class="d-flex flex-column pa-5">
            <span class="title product-name font-weight-regular">{{ item.item }}</span>
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
    </v-row>
  </v-container>
</template>
<script>
export default {
  data () {
    return {
      name: 1,
      items: ['one', 'two', 'three'],
      project: {
        name: '',
        sub_project_category: null,
        price: null,
        description: '',
        length: null,
        width: null,
        height: null,
        area: null,
        city: null
      },
      searchResults: [
        {
          id: 1,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 2,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 3,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 4,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 5,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 6,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 7,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 8,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 9,
          item: 'iPhone X 256 GB Black 2019 model'
        },
        {
          id: 10,
          item: 'iPhone X 256 GB Black 2019 model'
        }
      ]
    }
  },
  computed: {
    isMobile () {
      const { smAndDown } = this.$vuetify.breakpoint
      return smAndDown
    }
  },
  methods: {
  },
  mounted () {
    console.log('tr')
  }
}
</script>
<style lang="scss" scoped>
.main-wrapper {
  // background: #fff;
}
.v-input {
  // font-size: 14px;
}
.search-btn {
  border-top-right-radius: 7px;
  border-bottom-right-radius: 7px;
}
.product-name {
  line-height: 1.5rem;
}
.filters {
  // border-top-right-radius: 7px;
  // border-bottom-right-radius: 7px !important;
}

</style>
<style lang="scss">
.v-textarea textarea {
  padding: 0;
  margin: 0;
}
.main-search
.v-input__control,
.v-input__slot {
  // border-radius: 7px !important;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.filters.v-card {
  border-radius: 7px !important;
}
</style>
