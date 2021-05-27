<script lang="ts">
import { defineComponent, defineAsyncComponent, ref } from 'vue';

import streamSource from '@/streams.json';

const asyncStream = defineAsyncComponent(() => import('./components/Stream.vue'));

export default defineComponent({
  name: 'App',
  components: {
    asyncStream,
  },
  setup() {
    const streamCount = 9;
    const streams = ref([] as string[]);
    for (let i = 0; i < streamCount; i += 1) {
      streams.value.push(streamSource[Math.floor(Math.random() * streamSource.length)]);
    }
    return { streams };
  },
});
</script>

<template>
  <div class="container">
      <async-stream v-for="src in streams" class="stream" :src="src" :key="src" />
  </div>
</template>

<style lang="scss">
html { height: 100%; }
body { height: 100%; margin: 0; }

#app {
  height: 100%;
  width: 100vw;

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;

  background: black;

    .container {
      height: 100vh;
      width: 100vh;

      display: flex;
      flex-flow: row wrap;
      align-content: stretch;

      .stream {
        width: 30%;
        flex-grow: 1;
      }
    }
}
</style>
