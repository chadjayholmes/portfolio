<template>
  <div class="home" ref="hero">
    <div class="title">
      <div>Chad Holmes</div><div class="subtitle">Software Engineer & Web Developer</div>
    </div>
  </div>
</template>

<script>
import * as THREE from 'three'
import NET from "vanta/dist/vanta.net.min"

export default {
  name: 'Banner',
  components: {
  },
  mounted() {
    this.vantaEffect = NET({
      el: this.$refs.hero,
      THREE,
      mouseControls: false,
      touchControls: true,
      gyroControls: false,
      minHeight: 200.00,
      minWidth: 200.00,
      scale: 1.00,
      scaleMobile: 1.00,
      backgroundColor: 0x121212,
      color: 0x2776EA,
      points: 8.00,
      maxDistance: 20.00,
      spacing: 15.00
    })
  },
  beforeDestroy() {
    if (this.vantaEffect) {
      this.vantaEffect.destroy()
    }
  }
}
</script>

<style scoped>

.home{
  display: flex;
  height: 80vh;
  width: 100%;
}

.title{
  display: flex;
  flex-direction: column;
  width: 100%;
  color: white;
  font-weight: 900;
  align-items: flex-start;
  font-size: 72px;
  margin-top: auto;
  margin-bottom: auto;
  padding: 72px;
  border-radius: 10px;
}
.subtitle{
  display: flex;
  height: auto;
  margin-top: 10px;
  font-size: 42px;
  text-align: center;
  font-weight: bold;
}

@media only screen and (max-width: 1090px){

  .title{
    display: flex;
    flex-direction: column;
    width: 80%;
    margin-right: auto;
    margin-left: auto;
    align-items: center;
    font-size: 48px;
  }

  .subtitle{
    font-size: 24px;
  }
}
</style>