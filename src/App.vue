<template>
  <div>
    <Header />
    <div class="container">
      <Carousel />
      <Card />
      <Footer />
    </div>
  </div>
</template>

<script> 
import Footer from "./components/Copyrights.vue";
import Card from "./components/Card.vue";
import Carousel from "./components/Carousel.vue";
import Header from "./components/Header.vue";

export default {
  name: 'App',
  components: {
    Header,
    Carousel,
    Card,
    Footer
  }
};
</script>
