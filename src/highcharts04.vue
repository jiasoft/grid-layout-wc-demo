<script setup>
import {ref,onMounted} from "vue";
import Highcharts from 'highcharts';
import Highcharts3D from 'highcharts/highcharts-3d'
const chart = ref();
const chartOptions = ref( {
    chart: {
            type: 'pie',
            options3d: {
                    enabled: true,
                    alpha: 45,
                    beta: 0
            }
    },
    title: {
            text: '2014年某网站不同浏览器访问量占比'
    },
    tooltip: {
            pointFormat: '{series.name}: <b>{point.percentage:.1f}%</b>'
    },
    plotOptions: {
            pie: {
                    allowPointSelect: true,
                    cursor: 'pointer',
                    depth: 35,
                    dataLabels: {
                            enabled: true,
                            format: '{point.name}'
                    }
            }
    },
    series: [{
            type: 'pie',
            name: '浏览器占比',
            data: [
                    ['Firefox',   45.0],
                    ['IE',       26.8],
                    {
                            name: 'Chrome',
                            y: 12.8,
                            sliced: true,
                            selected: true
                    },
                    ['Safari',    8.5],
                    ['Opera',     6.2],
                    ['Others',   0.7]
            ]
    }]
});
onMounted(()=> {
    Highcharts3D(Highcharts)
    Highcharts.chart(chart.value,chartOptions.value)
})
</script>

<template>
<diV class="chart" ref="chart"></diV>

</template>

<style scoped>
.chart{
    width:100%;
    height: 100%;
}
</style>
