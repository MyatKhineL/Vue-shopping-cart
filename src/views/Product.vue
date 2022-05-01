<template>
  <div class="">
    <master>
      <Loader v-if="isLoad"></Loader>
      <div v-else class="container">
        <div class="row">
          <div v-for="p in products" :key="p.id" class="col-md-4">
            <div class="card">
              <div class="card-header">{{p.title}}</div>
              <div class="card-body">
                <img :src="p.image" width="100">
              </div>
              <div class="card-footer">
                <span>Price : <small>{{p.price}}</small></span>
                <a @click="addTocart(p)" class="btn btn-sm btn-dark float-end">Add to Cart</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </master>
  </div>

</template>

<script>
import Master from "@/views/Master";
import Loader from "@/components/Loader";
import axios from  'axios';


export default {
  components: {Loader, Master},
  data() {
    return {
      isLoad:true,
      products:[],



    }
  },
  created(){
        axios.get('https://fakestoreapi.com/products')
        .then(res=>{
           console.log(res.data)
           this.products = res.data;
           this.isLoad=false;
        });
  },
  methods: {
    addTocart(p) {
      var cart = this.globalArray;
      cart.push(p);
    }
  },
}
</script>

<style scoped>

</style>
