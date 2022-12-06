<template>
  <div></div>
</template>

<script>
export default {
  name: "PlayList",
  props: {
    songName: String,
    songArtist: String,
  },
  // METHODS
  methods: {
    addToPlaylist() {
      this.$emit(`addSong`, this.songName);
    },
  },
};
</script>

<style scoped>
</style>