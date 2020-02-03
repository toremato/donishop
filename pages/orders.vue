<template>
  <div>
    <div class="bg-test">
      <div class="test1" />
      <div class="test2" />
      <div class="foreground d-flex align-center">
        <v-container class="d-flex">
          <v-card class="pa-3 mr-7 border-20">
            <v-img class="border-10" width="9rem" height="9rem" :src="require('@/assets/santa.jpg')" />
          </v-card>
          <div class="d-flex flex-column justify-end">
            <div class="mb-8">
              <h1 class="white--text">Tore Maratov</h1>
            </div>
            <span class="headline"><strong>Email: </strong> tore.maratov@gmail.com</span>
            <span class="headline mb-n1"><strong>Телефон:</strong> +7-701-276-99-70</span>
          </div>
        </v-container>
      </div>
    </div>
    <v-container>
      <h1 class="display-1 font-weight-bold my-7">Мои Заказы</h1>
      <v-row>
        <v-col v-for="item in 8" :key="item" lg="3" md="4" sm="6">
          <v-card flat tile>
            <v-img height="220" class="grey lighten-2"></v-img>
            <div class="d-flex flex-column pa-5">
              <span class="title product-name font-weight-regular">iPhone X</span>
              <span class="title font-weight-bold">100,000 kzt</span>
              <span>Статус:</span>
              <div class="yellow">В Обработке</div>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>

export default {
  components: {
  }
}
</script>
<style lang="scss">
.bg-test {
  position: relative;
  height: 15rem;
  // background: yellow;
  .foreground {
    background: none;
    position: absolute;
    height: 100%;
    width: 100%;
    // background: cyan;
    .container {
      // height: 15rem;
    }
  }
  .test1 {
    height: 50%;
    width: 100%;
    position: absolute;
    background: rgb(135,103,242);
    background: linear-gradient(90deg, rgba(135,103,242,1) 50%, rgba(50,54,116,1) 100%);
  }
  .test2 {
    width: 100%;
    position: absolute;
    top: 50%;
    height: 50%;
    background: white;
  }
}
</style>
