<template>
  <div class="main-menu">
    <h1>{{ name }}</h1>
    <h2>Profile</h2>
    <ul>
      <li>
        <h3>Id</h3>
        <input type="text" v-model="currentPlayer.id" />
      </li>
      <li>
        <h3>Username</h3>
        <input type="text" v-model="currentPlayer.name" />
      </li>
    </ul>
    <h2>Options</h2>
    <ul>
      <li>
        <h3>Audio Volume {{ options.audioVolume }}</h3>
        <input type="range" v-model="options.audioVolume" />
      </li>
      <li>
        <h3>Sound Volume {{ options.soundVolume }}</h3>
        <input type="range" v-model="options.soundVolume" />
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: {
    player: {
      type: Object,
    },
  },

  data: function (data) {
    return {
      name: "Main Menu",
      currentPlayer: {
        id:
          this.player && this.player.id
            ? this.player.id
            : "No player id found?",
        name:
          this.player && this.player.name
            ? this.player.name
            : "No Player name found?",
      },
      options: {
        audioVolume: 50,
        soundVolume: 50,
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  font-size: 100%;
}
h3 {
  font-size: 110%;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
</style>
