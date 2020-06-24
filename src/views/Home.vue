<template>
  <div class="home">
    <div class="imageDiv">
      <img height="500" width="100%" :src="require('@/assets/main_image.png')">
      <div class="toolbar d-flex justify-space-between align-center px-4">
        <img class="logo" width="80" :src="require('@/assets/logo.png')">
        <div class="navigationLinks">
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About Us</a></li>
            <li><a href="#">Shop</a></li>
            <li><a href="#">Contact</a></li>
            <li>
              <v-btn icon color="black"><i class="bx bx-search-alt-2 "></i></v-btn>
            </li>
            <li>
              <v-btn icon color="black"><i class="bx bxs-lock-alt"></i></v-btn>
            </li>
          </ul>
        </div>
      </div>
      <div class="progress mr-6">
        <v-btn icon><i class="bx bx-checkbox"></i></v-btn>
        <v-btn icon><i class="bx bx-checkbox"></i></v-btn>
        <v-btn icon><i class="bx bx-checkbox"></i></v-btn>
        <v-btn icon><i class="bx bxs-checkbox"></i></v-btn>
      </div>
    </div>

    <div class="products my-12">
      <h3 class="text-center mb-4">POPULAR PRODUCTS</h3>
      <div class="cards d-flex justify-center">
        <div>
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

    <div class="gallery mt-12 mb-6 pa-5">
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
  </div>
</template>

<script>
export default {
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

.toolbar {
  width: 100%;
  position: absolute;
  top: 0;
  background: rgba(255, 255, 255, 0.5);
}

.progress {
  position: absolute;
  right: 2px;
  top: 30%;
}

.navigationLinks ul {
  list-style: none;
}

.navigationLinks ul li {
  display: inline-block;
  margin: 0 10px;
}

.navigationLinks ul li a {
  text-decoration: none;
  color: black;
}

.logo {
  position: relative;
  top: 1.5rem;
}

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
}
</style>