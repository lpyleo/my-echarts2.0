<template>
    <Charts :options="barChartOptionCreator()"></Charts>
</template>

<script setup>
import barChartOptionCreator from '@/charts/barChartOptions';
import Charts from './Charts.vue';


</script>

<style scoped>

</style>