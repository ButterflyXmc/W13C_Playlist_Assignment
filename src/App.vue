<template>
  <div id="app">
    <PageBody />
    <SongList />
    <PlayList />
  </div>
</template>

<script>
import PageBody from "@/components/PageBody.vue";
import PlayList from "@/components/PlayList.vue";
import SongList from "@/components/SongList.vue";
export default {
  name: "App",
  components: {
    PageBody,
    PlayList,
    SongList,
  },
};
</script>

<style>
html {
  background-color: black;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
