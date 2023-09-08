<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div id="app">
    <TablaPeriodica />
  </div>
</template>

<script>
import TablaPeriodica from "./TablaPeriodica.vue";

export default {
  components: {
    TablaPeriodica,
  },
};
</script>

<style scoped>



</style>
