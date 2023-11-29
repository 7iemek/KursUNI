<template>
  <div class="box">
    <div class="text">
      Zaraz nastąpi połączenie z konsultantem.
    </div>
    <div class="timer">
      <p v-if="countDown > 0">{{ countDown }}</p>
      <p v-else>Przepraszamy, może to potrwać dużej.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      countDown: 26,
      timer: null
    };
  },
  mounted() {
    this.startCountDown();
  },
  methods: {
    startCountDown() {
      this.timer = setInterval(() => {
        if (this.countDown > 0) {
          this.countDown--;
        } else {
          clearInterval(this.timer);
        }
      }, 1000);
    }
  },
  beforeUnmount() { 
    clearInterval(this.timer);
  }
};
</script>