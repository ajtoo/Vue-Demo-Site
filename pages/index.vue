<template>
  <section class="container">
    <navbar/>
    <image-slider/>
  </section>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import ImageSlider from '~/components/ImageSlider.vue'

export default {
  components: {
    Navbar,
    ImageSlider
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  align-items: center;
  text-align: center;
  flex-direction: column;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
