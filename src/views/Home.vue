<template>
  <BasicLayouts>
    <h2>Bienvenidos al Home</h2>
    <div class="ui horizontal list">
  <div class="item">
    <img class="ui mini circular image" src="../assets/elyse.png">
    <div class="content">
      <div class="ui sub header">Molly</div>
      Coordinador-Jhon Orozco 
    </div>
  </div>
  <div class="ui horizontal list">
  <div class="item">
    <img class="ui mini circular image" src="../assets/elyse.png">
    <div class="content">
      <div class="ui sub header">Molly</div>
      Developer-Yoan 
    </div>
  </div>
  <div class="item">
    <img class="ui mini circular image" src="../assets/elyse.png">
    <div class="content">
      <div class="ui sub header">Elyse</div>
      Scrum Master - Oswaldo Quiñones
    </div>
  </div>
  <div class="item">
    <img src="../assets/elyse.png" class="ui mini circular image">
    <div class="content">
      <div class="ui sub header">Eve</div>
      Project Manager-Gerardo Salcedo Pereira
    </div>
  </div>
</div>
  </BasicLayouts>
</template>

<script>
import BasicLayouts from '../layouts/BasicLayouts.vue';
export default {
  name: 'Home',
  components: {
    BasicLayouts,
  },
}
</script>
