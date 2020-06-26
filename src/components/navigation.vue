<template>
    <div class="navigation">
        <div class="imageDiv">
        <img height="500" width="100%" :src="require('@/assets/main_image.png')">
        <div class="toolbar d-flex justify-space-between align-center px-4">
          <img class="logo" to="/" width="80" :src="require('@/assets/logo.png')">
          <div class="navigationLinks hidden-sm-and-down">
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

          <div class="icons hidden-md-and-up">
            <v-btn class="mx-3" icon color="black"><i class="bx bx-search-alt-2 "></i></v-btn>
            <v-btn class="mx-3" icon color="black"><i class="bx bxs-lock-alt"></i></v-btn>
          </div>
          <!-- mobile nav -->
          <!-- hamburger menu -->
          <v-app-bar-nav-icon class="grey--text hidden-md-and-up" @click="drawer =!drawer"></v-app-bar-nav-icon>

          <v-navigation-drawer 
          color="#333"
          dark
          v-model="drawer"
          app
          class="hidden-md-and-up nav">
            <v-list>
              <v-list-tile>
                <v-list-tile-content>
                  <v-layout column>
                    <h3 class="text-center mb-4"></h3>
                    <v-btn class="text-center mx-4" text>Home</v-btn>
                    <v-btn  class="text-center mx-4" text>About Us</v-btn>
                    <v-btn  class="text-center mx-4" text>Shop</v-btn>
                    <v-btn class="text-center mx-4" text>Contact</v-btn>
                  </v-layout>
                </v-list-tile-content>
              </v-list-tile>
            </v-list>
          </v-navigation-drawer>
        </div>
        <div class="progress mr-6 hidden-sm-and-down">
          <v-btn icon><i class="bx bx-checkbox"></i></v-btn>
          <v-btn icon><i class="bx bx-checkbox"></i></v-btn>
          <v-btn icon><i class="bx bx-checkbox"></i></v-btn>
          <v-btn icon><i class="bx bxs-checkbox"></i></v-btn>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            drawer: false
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
  cursor: pointer;
}

</style>