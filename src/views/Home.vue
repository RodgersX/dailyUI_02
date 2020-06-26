<template>
  <div class="home">
    <div>
      <navigation-bar />
    </div>

    <div class="hidden-sm-and-down products my-12">
      <h3 class="text-center mb-4">POPULAR PRODUCTS</h3>
      <div class="cards d-flex justify-center">
        <div class="">
          <v-card
          class="card mx-2"
          width="250"
          v-for="(prod, i) in products"
          :key="i">
            <img width="250" :src="prod.img">
            <v-card-title>{{ prod.title }}</v-card-title>
            <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem?</v-card-text>
            <v-card-actions>
              <v-btn class="btns" text color="red">buy now</v-btn>
              <v-spacer></v-spacer>
              <v-card-text class="ml-12">$ {{ prod.price }}</v-card-text>
            </v-card-actions>
          </v-card>
        </div>
      </div>
    </div>

    <div class="hidden-md-and-up products my-12">
      <h3 class="text-center mb-4">POPULAR PRODUCTS</h3>
      <div class="cards d-flex justify-center">
        <div class="pa-4">
          <v-card
          class="card my-2"
          v-for="(prod, i) in products"
          :key="i">
            <img width="250" :src="prod.img">
            <v-card-title>{{ prod.title }}</v-card-title>
            <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem?</v-card-text>
            <v-card-actions>
              <v-btn class="btns" text color="red">buy now</v-btn>
              <v-card-text style="position: relative; left: 60%">$ {{ prod.price }}</v-card-text>
            </v-card-actions>
          </v-card>
        </div>
      </div>
    </div>

    <div class="hidden-sm-and-down gallery mt-12 mb-6 pa-5">
      <div class="pa-1" style="width: 60%">
        <img width="100%" height="100%" :src="require('@/assets/image_5.png')">
      </div>

      <div style="width: 40%" class="pa-1">
        <div class="why d-flex justify-center align-center mb-2" style="height: 50%">
          <div>WHY US</div>
        </div>
        <img height="48%" width="100%" :src="require('@/assets/image_4.png')">
      </div>
    </div>

    <div class="hidden-md-and-up pa-4">
      <div class="why d-flex justify-center align-center mb-2">
        <div>WHY US</div>
      </div>
      <img width="100%" height="240" :src="require('@/assets/image_5.png')">
      <img width="100%" height="240" :src="require('@/assets/image_4.png')">
    </div>
  </div>
</template>

<script>
import navigation from '@/components/navigation.vue'

export default {
  components: {
    'navigation-bar': navigation
  },
  data() {
    return {
      products: [
        {
          img: require('@/assets/image_3.png'),
          title: 'Rigstoni Pasta',
          // details: '',
          price: '43.00'
        },
        {
          img: require('@/assets/image_1.png'),
          title: 'Lumache Pasta',
          // details: '',
          price: '4.00'
        },
        {
          img: require('@/assets/image_2.png'),
          title: 'Cavatappi Pasta',
          // details: '',
          price: '56.00'
        }
      ]
    }
  }
}
</script>

<style scoped>

.card {
  display: inline-block;
}

.btns {
  text-transform: lowercase;
}

.gallery {
  height: 450px;
  display: flex;
  justify-content: space-between;
}

.why {
  background-image: url(../assets/image_6.png);
  background-size: cover;
  font-size: 25px;
  color: white;
  height: 200px;
}
</style>