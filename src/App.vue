<script lang="ts">
import { defineComponent } from 'vue';
import Stream from './components/Stream.vue';

export default defineComponent({
  name: 'App',
  components: {
    Stream,
  },
});
</script>

<template>
  <stream />
</template>

<style lang="scss">
html { height: 100%;}
body { height: 100%; margin: 0; }

#app {
  height: 100%;

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
