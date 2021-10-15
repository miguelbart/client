<template>
  <Basiclayouts>
    
      <img class="ui fluid image" src="../assets/sub-header-img.jpeg">
     
    <h1>Últimos productos</h1>
    <br>
    <div class="ui grid">
      <div class="sixten wide mobile eight wide tablet four wide computer column"
      v-for= "product in products"
      :key= "product.id"
      >

      <Product :product= "product" />
      </div>
    </div>
    <br>
     <Footer />
    
  </Basiclayouts>

  
</template>

<script>

import { ref, onMounted } from 'vue';
import Basiclayouts from '../layouts/Basiclayouts.vue';
import { getProducts } from '../api/product';
import Product from '../components/Product.vue';
import Footer from './Footer.vue'



export default {
  name: 'Home',



  components: {
    Basiclayouts,
    Product,
    Footer,
    
  },



  setup(){
    let products = ref(null);
    onMounted(async () => {
      const response = await getProducts(20);
      // console.log(response);
      products.value = response;
    });
    return {
      products,
    };
  },
  };
  



</script>

<style lang="scss" scoped>


h1{
  text-align: center;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

img{
  margin:0px;
  width:100%;
  
}
</style>



