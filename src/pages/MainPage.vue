<template>
  <div>
    <main>
      <video-background
        :src="video"
        style=" height: 100vh;"
        overlay="linear-gradient(45deg,#2a4ae430,#fb949e6b)"
        class="video"
      >
        <nav>
          <p>Home</p>
          <p>Contact</p>
          <p>About us</p>
        </nav>
        <h1 style="color: white; text-align: center;">
          The world is yours
        </h1>
      </video-background>
    </main>
  </div>
</template>

<script>
import VideoBackground from "vue-responsive-video-background-player";
import video from "../assets/video.mp4";
export default {
  name: "MainPage",
  components: { VideoBackground },
  data() {
    return {
      video,
    };
  },
};
</script>

<style scoped>
main {
  width: 100%;
  height: 100vh;
  margin: 0;
  padding: 0;
  background: black;
}

nav {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  font-size: 20px;
  width: 100%;
  color: white;
}
.video {
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: radial-gradient(
    farthest-corner at center center,
    #ce1a1a 0%,
    #ffffff 100%
  );
  font-size: 30px;
  font-family: Pompadur;
}
@font-face {
  font-family: Pompadur; /* Имя шрифта */
  src: url(../assets/18450.ttf); /* Путь к файлу со шрифтом */
}
</style>
