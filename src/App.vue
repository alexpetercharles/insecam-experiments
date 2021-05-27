<script lang="ts">
import { defineComponent, defineAsyncComponent } from 'vue';

const asyncStream = defineAsyncComponent(() => import('./components/Stream.vue'));

export default defineComponent({
  name: 'App',
  components: {
    asyncStream,
  },
});
</script>

<template>
  <div class="container">
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
      <async-stream class="stream" :src="'http://166.165.35.32/mjpg/video.mjpg'" />
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
