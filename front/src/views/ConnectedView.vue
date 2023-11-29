<template>
  <div class="box">
    <div class="text">
      Trwa połączenie...
    </div>
    <div class="timer">
      <p>Czas trwania połączenia: {{ connectionTime }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      connectionTime: 0,
      timer: null
    };
  },
  mounted() {
    this.startTimer();
  },
  methods: {
    startTimer() {
      this.timer = setInterval(() => {
        this.connectionTime++; // Zwiększaj czas połączenia co sekundę
      }, 1000);
    }
  },
  beforeUnmount() {
    clearInterval(this.timer); // Zatrzymaj licznik przy usuwaniu komponentu
  }
};
</script>