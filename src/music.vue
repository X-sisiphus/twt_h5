<template>
  <div>
    <div @click="changeOn" :class="isOff ? 'isOff' : 'isOn'"></div>
    <audio id="audio" :src="require('./assets/music.mp3')"></audio>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isOff: true,
    };
  },
  components: {},
  created() {},
  mounted() {
    // 自动播放音乐效果，解决微信自动播放问题
    document.addEventListener("touchstart", this.audioAutoPlay, false);
    document.addEventListener("WeixinJSBridgeReady", this.audioAutoPlay, false);
    let oAudio = document.querySelector("#audio");
    oAudio.onended = function () {
      //播放完毕，重新循环播放
      oAudio.load();
      oAudio.play();
    };
  },
  methods: {
    changeOn() {
      let oAudio = document.querySelector("#audio");
      if (this.isOff) {
        oAudio.play(); //开始播放
      } else {
        oAudio.pause(); //暂停播放
      }
      this.isOff = !this.isOff;
    },
    audioAutoPlay() {
      let audio = document.getElementById("audio");
      this.isOff = false;
      audio.play();
      document.removeEventListener("touchstart", this.audioAutoPlay);
    },
  },
};
</script>
 
<style scoped>
.isOn {
  width: 11%;
  height: 5%;
  position: fixed;
  z-index: 2000;
  top: 7.59%;
  right: 8.05%;
  background: url("./assets/music.png") no-repeat;
  background-size: 100% 100%;
}
@keyframes rotating {
  from {
    -webkit-transform: rotate(0);
  }
  to {
    -webkit-transform: rotate(360deg);
  }
}
@-webkit-keyframes rotating {
  from {
    -webkit-transform: rotate(0);
  }
  to {
    -webkit-transform: rotate(360deg);
  }
}
.isOff {
  width: 11%;
  height: 5%;
  position: fixed;
  z-index: 2000;
  top: 7.59%;
  right: 8.05%;
  background: url("./assets/unmusic.png") no-repeat;
  background-size: 100% 100%;
}
</style>