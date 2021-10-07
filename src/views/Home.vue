<template>
  <BasicLayouts>
    <h1>Nuestro equipo</h1>
    <div class="ui horizontal list">
      <div class="item">
        <img class="ui mini circular image" src="../assets/jhon.png">
          <div class="content">
            <div class="ui sub header">Jhon</div>
            Product Owner
            </div>
          </div>
      <div class="item">
        <img class="ui mini circular image" src="../assets/yohan.png">
          <div class="content">
            <div class="ui sub header">Yohan</div>
            Developer
            </div>
          </div>
      <div class="item">
        <img class="ui mini circular image" src="../assets/oswald.png">
          <div class="content">
            <div class="ui sub header">Oswald</div>
            Scrum Master
            </div>
          </div>
      <div class="item">
        <img src="../assets/gerard.png" class="ui mini circular image">
          <div class="content">
            <div class="ui sub header">Gerard</div>
            Project Manager
            </div>
          </div>
          <div class="item">
        <img class="ui mini circular image" src="../assets/oswald.png">
          <div class="content">
            <div class="ui sub header">Mike</div>
            QA Enginner
            </div>
          </div>
        </div>
        <br><br>
        <h1>Colecciones</h1>
<h1>Uniforme de Gala</h1>
<div class="ui three column grid">
  <div class="column">
    <div class="ui segment">
      <img src="../assets/bleiser.jpg">
      <div class="ui sub header">Blazers - Chaquetas</div>
        <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
  </div>
    </div>
  </div>
  <div class="column">
    <div class="ui segment">
      <img src="../assets/shirt.jpg">
      <div class="ui sub header">Camisas</div>
      
  <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
  </div>

    </div>
  </div>
  <div class="column">
    <div class="ui segment">
      <img src="../assets/skirt.jpg">
      <div class="ui sub header">Faldas</div>
        <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
  </div>
    </div>
  </div>
</div>

<h1>Uniforme deportivo</h1>
<div class="ui three column grid">
  <div class="column">
    <div class="ui segment">
      <img src="../assets/deportivo.jpeg">
      
      <div class="ui sub header">Camisetas</div>
        <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
  </div>
      </div>
      <div class="ui segment">
        <img src="../assets/deportivo.jpeg">
        <div class="ui sub header">chaquetas</div>
        <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
    </div>
    </div>
      
  </div>
  <div class="column">
    <div class="ui segment">
      <img src="../assets/sudadera.jpeg">
      <div class="ui sub header">Sudadera</div>
      
  <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
  </div>

    </div>
  </div>
  <div class="column">
    <div class="ui segment">
      <img src="../assets/camiseta_sudadera.jpeg">
      <div class="ui sub header">Pantalonetas</div>
        <div class="ui two bottom attached buttons">
    <div class="ui button">
      <i class="add icon"></i>
      Agregar
    </div>
    <div class="ui primary button">
      <i class="play icon"></i>
      Ver mas
    </div>
  </div>
    </div>
  </div>
</div>
  
        <h1>Últimos productos</h1>
    <div class="ui grid">
      <div
        class="sixten wide mobile eight wide tablet four wide computer column"
        v-for="product in products"
        :key="product.id"
      >
        <Product :product="product" />
      </div>
    </div>
  </BasicLayouts>
</template>

<script>
import { ref, onMounted } from 'vue';
import BasicLayouts from '../layouts/BasicLayouts.vue';
import { getProducts } from '../api/products';
import Product from '../components/Product.vue';
export default {
  name: 'Home',
  components: {
    BasicLayouts,
    Product,
  },

  setup() {
    let products = ref(null);

    onMounted(async () => {
      const response = await getProducts(20);
      products.value = response;
    });
    return {
      products,
    };
  },
};
</script>
