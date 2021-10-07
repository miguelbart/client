<template>
  <BasicLayouts>
    <h2>Este es el Home</h2>
    <div class="ui horizontal list">
  <div class="item">
    <img class="ui mini circular image" src="../assets/jhon.png">
    <div class="content">
      <div class="ui sub header">Jhon</div>
      Coordinador-Jhon Orozco 
    </div>
  </div>
<div class="ui horizontal list">
  <div class="item">
    <img class="ui mini circular image" src="../assets/yohan.png">
    <div class="content">
      <div class="ui sub header">Yohan</div>
      Developer Yohan
    </div>
  </div>
  <div class="item">
    <img class="ui mini circular image" src="../assets/oswald.png">
    <div class="content">
      <div class="ui sub header">Oswaldo</div>
      Scrum Master - Oswaldo Quiñones
    </div>
  </div>
  <div class="item">
    <img src="../assets/gerard.png" class="ui mini circular image">
    <div class="content">
      <div class="ui sub header">Gerardo</div>
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
