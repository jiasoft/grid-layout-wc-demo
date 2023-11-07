<script setup>
import { ref, onMounted } from "vue";
import Highcharts from 'highcharts';
import Highcharts3D from 'highcharts/highcharts-3d'
const chart = ref();
const chartOptions = ref({
        chart: {
                type: 'pie',
                options3d: {
                        enabled: true,
                        alpha: 45
                }
        },

        plotOptions: {
                pie: {
                        innerSize: 100,
                        depth: 45
                }
        },
        series: [{
                name: '货物金额',
                data: [
                        ['香蕉', 8],
                        ['猕猴桃', 3],
                        ['桃子', 1],
                        ['橘子', 6],
                        ['苹果', 8],
                        ['梨', 4],
                        ['柑橘', 4],
                        ['橙子', 1],
                        ['葡萄 (串)', 1]
                ]
        }]
});
onMounted(() => {
        Highcharts3D(Highcharts)
        Highcharts.chart(chart.value, chartOptions.value)
})
</script>

<template>
        <diV class="chart" ref="chart"></diV>
</template>

<style scoped>
.chart {
        width: 100%;
        height: 100%;
}
</style>
