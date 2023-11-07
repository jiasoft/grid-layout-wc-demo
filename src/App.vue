<script setup>
import 'grid-layout-wc/grid-layout-wc.js';
import highcharts01 from "./highcharts01.vue";
import highcharts02 from "./highcharts02.vue";
import highcharts03 from "./highcharts03.vue";
import highcharts04 from "./highcharts04.vue"
import highcharts05 from "./highcharts05.vue"
const layoutList = [
{x: 1, y: 1, w: 44, h: 40,"slot":"1","id":1},
{x: 46, y: 1, w: 81, h: 40,"slot":"2","id":2},
{x: 1, y: 42, w: 69, h: 35,"slot":"3","id":3},
{x: 71, y: 42, w: 56, h: 35,"slot":"4","id":4},
{x: 1, y: 55, w: 37, h: 34,"slot":"5","id":5,float: true}
]

</script>

<template>

  <main>
    <grid-layout-wc :layoutData="layoutList" :edit="true">
      <div slot="1">
        <highcharts01 />
      </div>
      <div slot="2">
        <highcharts02 />
      </div>
      <div slot="3" >
        <highcharts03 />
      </div>
      <div slot="4" >
        <highcharts04 />
      </div>
      <div slot="5">
        <highcharts05 />
      </div>
    </grid-layout-wc>
  </main>
</template>

<style scoped>
main {
  width:1280px;
  margin:auto;
  height: 100vh;
}
</style>
