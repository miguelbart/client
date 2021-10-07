<template>
  <BasicLayouts>
    <h2>Este es el Home</h2>
    <div class="ui horizontal list">
  <div class="item">
    <img class="ui mini circular image" src="../assets/elyse.png">
    <div class="content">
      <div class="ui sub header">Molly</div>
      Coordinator-Jhon Orozco
    </div>
  </div>
<div class="ui horizontal list">
  <div class="item">
    <img class="ui mini circular image" src="../assets/elyse.png">
    <div class="content">
      <div class="ui sub header">Connor</div>
      Developer Yohan
    </div>
  </div>
  <div class="item">
    <img class="ui mini circular image" src="../assets/elyse.png">
    <div class="content">
      <div class="ui sub header">Elyse</div>
      Oswaldo
    </div>
  </div>
  <div class="item">
    <img src="../assets/elyse.png" class="ui mini circular image">
    <div class="content">
      <div class="ui sub header">Eve</div>
      Project Manager-Gerardo Salcedo
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
