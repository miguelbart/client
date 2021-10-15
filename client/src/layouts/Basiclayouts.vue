<template>
<div>
  <div class="Basic-layout">
      <Menu/>
    
    <div class="ui container">
      <slot />
  </div>
  </div>
  <Cart />
  </div>
</template>

<script>
import Menu from '../components/menu.vue';
import Cart from '../components/Cart/Cart.vue'
export default {
    name: "Basiclayouts",
    components: {
        Menu,
        Cart,
    
        },
};

</script>

<style>

</style>