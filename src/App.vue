<template>
  <div class="wrapper">
    <BarChart class="chart"></BarChart>
  </div>
</template>

<script setup>
import BarChart from './components/BarChart.vue';
</script>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
.wrapper {
  width: 100vw;
  height: 100vh;
}
.wrapper .chart {
  width: 50%;
  height: 90%;
}</style>