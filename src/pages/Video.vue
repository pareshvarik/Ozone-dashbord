<template>
  <div id="player">
    <div class="test-player-wrap">
      <vue-core-video-player
        loop
        :src="source"
        title="Video Player"
        autoplay
      ></vue-core-video-player>
    </div>
    <button @click="change">Change Source</button>
  </div>
</template>

<script>
const videoSource = [
  {
    src:
      "https://media.vued.vanthink.cn/y2mate.com%20-%20Sparkle%20_%20Your%20Name%20AMV_K_7To_y9IAM_240p.mp4",
    resolution: "240p",
  },
];
const videoSource2 =
  "https://media.vued.vanthink.cn/the_garden_of_words_trailer_english__1080p.mp4";
const cover = "https://img1.wxzxzj.com/maxresdefault.jpg";

export default {
  name: "Video",
  data() {
    return {
      source: videoSource2,
      cover: cover,
    };
  },
  methods: {
    change() {
      this.source = videoSource;
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#app .vue-core-video-player-containers {
  margin: 60px auto;
}
#app .test-player-wrap {
  width: 720px;
  height: 405px;
  position: relative;
  margin: 80px auto;
}
</style>