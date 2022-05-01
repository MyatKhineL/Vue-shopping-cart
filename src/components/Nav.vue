<template>
  <div>
    <nav class="navbar navbar-expand-lg  bg-dark">
      <div class="container-fluid">

        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">

            <li class="nav-item">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/product">Product</router-link>
            </li>



          </ul>
          <div class="nav-item">
            <router-link class="nav-link" to="cart">
              <i class="fas fa-shopping-cart text-white"></i>
              <small class="badge badge-danger bg-danger">0</small>
            </router-link>
          </div>


        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

</style>