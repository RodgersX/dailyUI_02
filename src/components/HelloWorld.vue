<template>
  <div class="hello">
    <div>
      <img height="450" width="100%" :src="require('@/assets/main_image.png')">
      <nav class="navbar navbar-expand-lg navbar-light">
        <a href="#" class="navbar-brand">
          <img width="60" :src="require('@/assets/logo.png')">
        </a>

        <!-- navigation bar -->
        <div class="navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ml-auto mr-3">
            <li class="nav-item active">
              <a href="#" class="nav-link">Home</a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">About Us</a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">Shop</a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">Contact</a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link"><i class="bx bxs-lock-alt"></i></a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link"><i class="bx bx-search"></i></a>
            </li>
          </ul>
        </div>
      </nav>
    </div>

    <!-- popular products -->
    <div class="container my-5">
      <h3 class="text-center mb-5">POPULAR PRODUCTS</h3>
      <div class="row">
        <div class="col"
        v-for="prod in products"
        :key="prod.id">
          <div 
          class="card" 
          style="width:18rem;">
            <img :src="prod.img" class="card-img-top">
            <div class="card-body">
              <h5 class="card-title">{{ prod.title }}</h5>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <div class="form-inline">
                <a href="#" class="card-link text-danger">buy now</a>
                <p class="card-link ml-auto">$ {{ prod.price }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- fluid grid  -->
    <div class="images">
      
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {  
      products: [
        {img: require('@/assets/image 3.png'), title: 'Rigatoni Pasta', price: '43.00'},
        {img: require('@/assets/image 2.png'), title: 'Lumache Pasta', price: '4.00'},
        {img: require('@/assets/image 1.png'), title: 'Cavatappi Pasta', price: '56.00'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.navbar {
  position: absolute;
  top: 0;
  width: 100%;
  height: 70px;
  background: rgba(255,255,255,0.6);
}

.navbar-brand {
  position: relative;
  top: 1.5rem;
}

</style>
