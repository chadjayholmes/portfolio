<template>
  <div>
    <Slide right>
      <a id="home" href="#">
        <span>Home</span>
      </a>
      <a id="Projects" href="#">
        <span>Projects</span>
      </a>
      <a id="Experience" href="#">
        <span>Experience</span>
      </a>
    </Slide>
  </div>
</template>

<script>
import { Slide } from "vue-burger-menu";

export default {
  data() {
    return {
      open: false
    };
  },
  methods: {
    openMenu() {
      this.open = true;
    }
  },
  components: {
    Slide
  }
};
</script>

<style>

.bm-burger-bars {
  background-color: white;
}

</style>