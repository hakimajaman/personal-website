<template>
  <section-1 />
  <section-2 />
  <section-3 />
  <section-4 />
  <section-5 />
  <section-6 />
  <Footer />
</template>

<script>
import Section1 from "./components/Section1.vue";
import Section2 from "./components/Section2.vue";
import Section3 from "./components/Section3.vue";
import Section4 from "./components/Section4.vue";
import Section5 from "./components/Section5.vue";
import Section6 from "./components/Section6.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
    Section6,
    Footer
  }
};
</script>

<style>
body,
html {
  padding: 0;
  margin: 0;
  width: 100%;
  min-height: 100vh;
  overflow-x: hidden;
}
body {
  background-color: #20194a;
}
</style>
