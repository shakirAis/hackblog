<template>
  <div class="wrapper">
    <Header />
    <Banner />
    <Posts />
    <Footer />
  </div>
</template>

<script>
import Header from "~/components/Header.vue";
import Footer from "~/components/Footer.vue";
import Banner from "~/components/Banner.vue";
import Posts from "~/components/Posts.vue";

export default {
  components: {
    Header,
    Footer,
    Banner,
    Posts
  },
};
</script>

<style>
body, html {
  width: 100%;
  height: auto;
  margin: 0;
  position: relative;
}
.wrapper {
  width: 100%;
  height: auto;
  margin: 0;
  position: relative;
}
</style>
