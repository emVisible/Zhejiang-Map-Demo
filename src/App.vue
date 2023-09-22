<script setup lang="ts">
import { ref } from 'vue';
import changeType from './components/changeType.vue';
import Source from './components/rawMap.vue';
import Back from './components/back.vue';
import Map from './view/map/index.vue';


const type = ref("")
function handleChange(value: string) {
  type.value = value
}

</script>

<template>
  <div class="root">
    <section>
      <h1>地图Demo</h1>
      <Map :type="type" />
    </section>
    <section>
      <h1>源数据</h1>
      <Source />
    </section>
    <section>
      <Back />
      <changeType @state="handleChange" />
    </section>
  </div>
</template>

<style scoped lang="scss">
.root {

  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
