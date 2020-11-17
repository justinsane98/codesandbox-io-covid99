<template>
  <div class="player">
    <h1>{{ name }}</h1>
  </div>
</template>
<script>
export default {
  name: "player",
  data: function () {
    return {
      name: "Player",
      player: {
        id: 0,
        username: "Null Heiress",
      },

      options: {
        audioVolume: 50,
        soundVolume: 50,
      },
    };
  },
};
</script>
