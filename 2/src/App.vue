<template>
  <div id="app">
    <HeaderComponent></HeaderComponent>
    <div class="top-banner">
      <section class="blog-details__intro">
        <img src="./assets/blog-details-intro.png" alt="photo">
      </section>
    </div>
    <div id="blog-details" class="blog-details center">
      <blogsDetails></blogsDetails>
    </div>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import blogsDetails from './components/blogsDetails.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    blogsDetails,
    HeaderComponent,
    FooterComponent,

  }
}
</script>

<style scoped>
.top-banner {
  margin-bottom: 50px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: center;
  min-height: 351px;
  max-width: 500px;
}
</style>
