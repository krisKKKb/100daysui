<template>
  <div>
    <h2>Countdown timer</h2>
    <h1>{{ parseSeconds(countDown) }}</h1>
    <div>
      <button type="button" @click="rem(3600)">- hr</button>
      <button type="button" @click="add(3600)">+ hr</button>
      <button type="button" @click="rem(60)">- min</button>
      <button type="button" @click="add(60)">+ min</button>
      <button type="button" @click="rem(1)">- s</button>
      <button type="button" @click="add(1)">+ s</button>
    </div>
    <div>
      <button type="button" @click="setRunning(true)">Start</button>
      <button type="button" @click="setRunning(false)">Stop</button>
      <button type="button" @click="reset()">Reset</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      countDown: 60,
      running: false,
    };
  },
  methods: {
    setRunning(bool) {
      this.running = bool;
    },
    parseSeconds(seconds) {
      return new Date(seconds * 1000).toISOString().substr(11, 8);
    },
    countDownTimer() {
      if (this.countDown > 0 && this.running) {
        setTimeout(() => {
          this.countDown > 0 ? (this.countDown -= 1) : 0;
          this.countDownTimer();
        }, 1000);
      }
      if (this.countDown <= 0) {
        this.running = false;
      }
    },
    add(sec) {
      this.countDown += parseInt(sec);
    },
    rem(sec) {
      if (this.countDown >= parseInt(sec)) {
        this.countDown -= parseInt(sec);
      }
    },
    reset() {
      this.running = false;
      this.countDown = 0;
    },
  },
  watch: {
    running: function () {
      this.countDownTimer();
    },
  },
  created() {},
};
</script>

<style scoped>
.img {
  width: 300px;
  height: auto;
}
</style>
