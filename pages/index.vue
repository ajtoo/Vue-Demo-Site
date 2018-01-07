<template>
  <section class="container">
    <navbar/>
    <image-slider/>
    <headline-c-t-a/>
    <section class="note-row">
      <div class="sm-col-6">
        <note/>
      </div>
      <div class="sm-col-6">
        <note/>
      </div>
    </section>
    <section class="note-row">
      <div class="sm-col-6">
        <note/>
      </div>
      <div class="sm-col-6">
        <note/>
      </div>
    </section>
  </section>
</template>

<script>

import Navbar from '~/components/Navbar.vue'
import ImageSlider from '~/components/ImageSlider.vue'
import HeadlineCTA from '~/components/HeadlineCTA.vue'
import Note from '~/components/Note.vue'

export default {
  components: {
    Navbar,
    ImageSlider,
    HeadlineCTA,
    Note
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

.sm-col-6 {
  width: 50%;
  position: relative;
  padding: .5em 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.note-row {
  width: 100%;
  align-items: center;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

@media (max-width: 768px) {
  [class*="sm-col"] {
    width: 100%
  }

  .note-row {
    flex-direction: column;
  }
}

</style>
