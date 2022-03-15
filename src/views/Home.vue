<template>
  <div>
    <Nav class="nav"/>
    <Banner class="banner"></Banner>
    <AboutRow/>
  </div>
</template>

<script>
import Nav from "@/components/Nav"
import Banner from "@/components/Banner";
//import ProjectsRow from "@/components/ProjectsRow";
import AboutRow from "@/components/AboutRow";

export default {
  data() {
    return {
      open: false,
    };
  },
  methods: {
    openMenu() {
      this.open = true;
    }
  },
  name: 'Home',
  components: {
    AboutRow,
    //ProjectsRow,
    Banner,
    Nav
  },
}
</script>

<style scoped>


.banner{
  padding-bottom: 25px;
  z-index: -1;
}

</style>
