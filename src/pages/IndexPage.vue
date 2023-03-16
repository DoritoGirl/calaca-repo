<template>
  <div class="main">
    <div class="skull-btn" v-if="calaca == false">
      <h1>Click here to party</h1>
      <q-btn round @click="activateCalca()">
        <q-avatar size="250px">
          <img src="../assets/img/19654.jpg">
        </q-avatar>
      </q-btn>
    </div>
    <div v-if="calaca === true" class="vid">
      <video loop width=" 320" height="240" controls autoplay volume="0.45">
        <source src="../assets/vid/Skull_Trumpet.mp4" type="video/mp4">
      </video>

    </div>
  </div>
</template>

<script>

export default ({
  name: 'IndexPage',
  data() {
    return {
      calaca: false,
    }
  },

  methods: {
    activateCalca() {
      return this.calaca = true
    },

  }
})
</script>

<style lang="scss">
@font-face {
  font-family: "Pacific";
  src: url(./font/Pacifico-Regular.ttf);
}

* {}

.main {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: black;

  video {
    width: 900px;
    height: auto;
  }
}

.skull-btn {
  margin: 50px 0px 50px 0px;
  display: flex;
  align-items: center;
  flex-direction: column;

  .q-btn {}

  h1 {
    color: #fff;
    font-size: 70px;
    font-weight: 100;
    font-family: "Pacific";
    margin-bottom: 50px;
    line-height: 1;
    animation: text-flicker 5s linear infinite;
    text-shadow: 2px 2px 1px rgba(0, 0, 0, .4),
      0 0 20px #fe3a80,
      0 0 40px rgba(255, 0, 91, .75),
      0 0 50px rgba(255, 0, 91, .75),
      0 0 100px rgba(255, 0, 91, .75);
  }
}
</style>