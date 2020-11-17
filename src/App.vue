<template>
  <div class="container">
    <main>
      <!-- NEXT UP!!!! send a username and ID to the canvas and display it -->
      <canvas></canvas>
    </main>
    <aside>
      <MainMenu v-bind:player="currentPlayer" />
    </aside>
  </div>
</template>

<script>
import guid from "guid";
import MainMenu from "./components/MainMenu.vue";
export default {
  name: "App",
  props: {
    player: Object,
  },
  components: {
    MainMenu: MainMenu,
  },
  computed: {
    guid() {
      return guid.create();
    },
    currentPlayer() {
      return {
        id: guid.create(),
        name: "Testing",
      };
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  margin: 10px;
  overflow: hidden;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.container {
  display: flex;
}
canvas {
  border: 1px solid red;
  width: 600px;
  height: 480px;
}
aside {
  flex-grow: 1;
}
</style>
