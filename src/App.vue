<script setup>
import 'grid-layout-wc/grid-layout-wc.js';
const layoutList = [
  {x:1,y:1,w:20,h:12,slot:"1",id:1},
  {x:22,y:1,w:20,h:12,slot:"2",id:2},
  {x:43,y:1,w:30,h:12,slot:"3",id:3}
]
</script>

<template>

  <main>
    <grid-layout-wc :layoutData="layoutList" :edit="true">
      <div slot="1" style="background-color: rgb(217, 202, 229);margin-top: 30px;">
        {x:1,y:1,w:20,h:12,slot:"1"}
      </div>
      <div slot="2" style="background-color: rgb(193, 205, 236);margin-top: 30px;">
        {x:1,y:1,w:20,h:12,slot:"2"}
      </div>
      <div slot="3" style="background-color: rgb(178, 212, 197);margin-top: 30px;">
        {x:1,y:1,w:20,h:12,slot:"2"}
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
