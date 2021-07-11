<template>
  <div class="wave-container">
    <div class="wave"></div>
  </div>
</template>

<script>
export default {
  setup () {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/anims.scss';
.wave-container {
  position: relative;
  background-color: #2A73FE;
  width: 200px;
  height: 150px;
  margin: 0 auto;
}

.wave {
  position: absolute;
  bottom: 60%;
  width: 200px;
  height: 100px;
  overflow: hidden;
}
.wave::before {
  content: "";
  background-color: #fff;
  opacity: 0.5;
  border-radius: 40%;
  position: absolute;
  left: -75%;
  bottom: 25%;
  width: 500px;
  height: 500px;
  animation: spin 8s linear infinite;
}

.wave::after {
  content: "";
  background-color: #fff;
  opacity: 0.5;
  border-radius: 40%;
  position: absolute;
  left: -75%;
  bottom: 25%;
  width: 500px;
  height: 500px;
  animation: spin 10s linear infinite;
}
</style>