<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Sketch',
  props: {
    src: {
      type: String,
      required: true,
    },
  },
});
</script>

<template>
  <div class="stream">
    <img :src="src" />
  </div>
</template>

<style lang="scss" scoped>
.stream {
  img {
    height: 100%;
    width: 100%;
    object-fit: cover;
  }
}
</style>
