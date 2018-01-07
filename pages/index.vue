<template>
  <section class="container">
    <navbar/>
    <image-slider/>
    <headline-c-t-a/>
    <section class="content-row">
      <div class="sm-col-6">
        <note/>
      </div>
      <div class="sm-col-6">
        <note/>
      </div>
    </section>
    <section class="content-row">
      <div class="sm-col-6">
        <note/>
      </div>
      <div class="sm-col-6">
        <note/>
      </div>
    </section>
    <angled-banner/>
    <h1 class="section-heading"><span class="orange-text">Lorem</span> Ipsum</h1>
    <section class="content-row stats">
      <figure class="stat">
        <animated-number :number="240"/>
        <p class="light-orange-text">Lorem ipsum dolor sit amet Lorem ipsum dolor ipsum dolor</p>
      </figure>
      <figure class="stat">
        <animated-number :number="150"/>
        <p class="light-orange-text">Lorem ipsum dolor sit amet Lorem ipsum dolor ipsum dolor</p>
      </figure>
      <figure class="stat">
        <animated-number :number="509"/>
        <p class="light-orange-text">Lorem ipsum dolor sit amet Lorem ipsum dolor ipsum dolor</p>
      </figure>
    </section>
    <h1 class="section-heading"><span class="orange-text">Lorem</span> Ipsum</h1>
  </section>
</template>

<script>

import Navbar from '~/components/Navbar.vue'
import ImageSlider from '~/components/ImageSlider.vue'
import HeadlineCTA from '~/components/HeadlineCTA.vue'
import Note from '~/components/Note.vue'
import AngledBanner from '~/components/AngledBanner.vue'
import AnimatedNumber from '~/components/AnimatedNumber.vue'

export default {
  components: {
    Navbar,
    ImageSlider,
    HeadlineCTA,
    Note,
    AngledBanner,
    AnimatedNumber
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

.content-row {
  width: 100%;
  align-items: center;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.section-heading {
  margin-top: 8rem;
  font-size: 2rem;
}

.orange-text {
  color: #f76b1c;
}

.light-orange-text {
  color: #f3b160;
}

.stats {
  justify-content: space-around;
}

.stat {
  font-weight: bold;
  width: 15vw;
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
