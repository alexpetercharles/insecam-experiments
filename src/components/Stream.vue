<script lang="ts">
import { defineComponent, onMounted, ref } from 'vue';

export default defineComponent({
  name: 'Sketch',
  setup() {
  },
});
</script>

<template>
  <div ref="container" class="container" />
</template>

<style lang="scss" scoped>
.container {
  height: 100%;
  width: 100%;
}
</style>
