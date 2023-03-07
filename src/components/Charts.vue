<template>
    <div class="container" ref="container"></div>
</template>

<script setup>
    import { ref, onMounted, watch, toRefs } from 'vue';
    import * as echarts from 'echarts';

    const container = ref(null)
    const chart = ref(null)
    const props = defineProps({
        options: {
            required: true,
            type: Object,
            default: {}
        }
    })
    const { options } = toRefs(props)
    watch(
        options,
        (newOptions) => {
            chart.value.setOption(newOptions)
        },
        {
            deep: true
        }
    )
    onMounted(() => {
        chart.value = echarts.init(container.value)
        chart.value.setOption(props.options)
    })
</script>

<style scoped>
    .container {
        width: 100%;
        height: 100%;
    }
</style>