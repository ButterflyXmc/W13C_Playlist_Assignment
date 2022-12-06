<template>
  <div>
    <main v-for="song in songs" :key="song">
      <img :src="song.img" />
      <h3>{{ song.song }}</h3>
      <i
        >{{ song.artist }} <br />
        <button>Select</button></i
      >
    </main>
    <PlayList
      v-for="(song, index) in songs"
      :key="index"
      :songName="song.song"
      :songArtist="song.artist"
      @addSong="listenToIt"
    />
  </div>
</template>

<script>
import PlayList from "@/components/PlayList.vue";

export default {
  components: {
    PlayList,
  },

  name: "PageBody",
  data() {
    return {
      playlist: [],
      songs: [
        {
          img: "https://i.scdn.co/image/ab67616d0000b273da5b9c1eb275d48e14d25f3e",
          song: "Verdansk",
          artist: "Dave",
        },
        {
          img: "https://i.scdn.co/image/ab67616d0000b273c8eaf2ad9b478ea68c0370a5",
          song: "Stylin'",
          artist: "Sainté",
        },
        {
          img: "https://i.scdn.co/image/ab67616d0000b2739c8890c824bb9be2360e79c1",
          song: "Sin Pijama",
          artist: "Becky G",
        },
        {
          img: "https://musicchartsarchive.com/sites/default/files/albums/cole-j--off-season.jpg",
          song: "Amrai",
          artist: "J.Cole",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/en/d/df/DaveFredoFunkyFriday.png",
          song: "Funky Friday",
          artist: "Dave",
        },
        {
          img: "https://i.scdn.co/image/ab67616d0000b27346a2fa2ff08740df703a9ac0",
          song: "Very Few Friends",
          artist: "Saint Levant",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/en/a/aa/Dave_-_Clash.jpeg",
          song: "Clash",
          artist: "Dave",
        },
      ],
    };
  },
  methods: {
    ListenToIt(song) {
      this.playlist.push(song);
    },
  },
};
</script>


<style scoped>
img {
  height: 20vh;
}

main {
  color: white;
  border: white solid 2px;
  width: 30%;
  position: relative;
  left: 50%;
  transform: translate(-50%);
  padding: 20px;
  background-color: rgba(245, 245, 245, 0.159);
  margin: 30px;
}

button {
  background-color: rgb(116, 116, 128);
  color: rgba(245, 245, 245, 0.755);
  border: rgba(255, 255, 255, 0.472) 1px solid;
}
</style>