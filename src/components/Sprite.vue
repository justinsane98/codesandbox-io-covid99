<template>
  <svg xmlns="http://www.w3.org/2000/svg">
    <use
      xmlns:xlink="http://www.w3.org/1999/xlink"
      xlink:href="spritePath"
    ></use>
  </svg>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
  },
  computed: {
    spritePath() {
      return "/assets/sprite.svg" + "#" + this.name;
    },
  },
};
</script>