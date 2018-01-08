<template>
  <section class="container">
    <navbar/>
    <button id="contact" @click="showModal = true"/>
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
    <h1 class="section-heading spacing-below"><span class="orange-text">Lorem</span> Ipsum</h1>
    <section class="content-row spacing-below">
      <div class="sm-col-6">
        <p class="text-paragraph">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ellamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur
        </p>
      </div>
      <div class="sm-col-6">
        <button class="cta" @click="buttonClicked">Button</button>
      </div>
    </section>
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
    <h1 class="section-heading spacing-below"><span class="orange-text">Lorem</span> Ipsum</h1>
    <section class="content-row spacing-below">
      <div class="sm-col-6">
        <h4 class="orange-text paragraph-header">Lorem ipsum dolor sit amet</h4>
        <h5 class="light-orange-text paragraph-header spacing-below">Lorem ipsum dolor sit amet lorem</h5>
        <p class="text-paragraph">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ellamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur
        </p>
      </div>
      <div class="sm-col-6">
        <img class="row-image" src="https://res.cloudinary.com/ajhtoo/image/upload/v1515176157/img1_jxgi73.jpg"/>
      </div>
    </section>
    <section class="content-row spacing-below reverse-stack">
      <div class="sm-col-6">
        <img class="row-image" src="https://res.cloudinary.com/ajhtoo/image/upload/v1515176157/img2_m4defs.jpg"/>
      </div>
      <div class="sm-col-6">
        <h4 class="orange-text paragraph-header">Lorem ipsum dolor sit amet</h4>
        <h5 class="light-orange-text paragraph-header spacing-below">Lorem ipsum dolor sit amet lorem</h5>
        <p class="text-paragraph">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ellamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur
        </p>
      </div>
    </section>
    <modal v-if="showModal" @close="showModal = false"/>
  </section>
</template>

<script>

import Navbar from '~/components/Navbar.vue'
import ImageSlider from '~/components/ImageSlider.vue'
import HeadlineCTA from '~/components/HeadlineCTA.vue'
import Note from '~/components/Note.vue'
import AngledBanner from '~/components/AngledBanner.vue'
import AnimatedNumber from '~/components/AnimatedNumber.vue'
import Modal from '~/components/Modal.vue'

export default {
  components: {
    Navbar,
    ImageSlider,
    HeadlineCTA,
    Note,
    AngledBanner,
    AnimatedNumber,
    Modal
  },
  data: function () {
    return {
      showModal: false
    }
  },
  methods: {
    buttonClicked () {
      alert('fill in your button click function here')
    }
  }
}
</script>

<style>
h4 {
  font-size: 1.75rem;
}
h5 {
  font-size: 1.5rem;
}
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
  flex-direction: column;
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

.medium-orange-text {
  color: #e49535;
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

.paragraph-header {
  width: 85%;
  text-align: left;
}

.text-paragraph {
  text-align: left;
  width: 85%;
}

.spacing-below {
  margin-bottom: 3rem;
}

.row-image {
  max-width: 100%;
}

.reverse-stack {

}

@media (max-width: 768px) {
  [class*="sm-col"] {
    width: 100%
  }

  .note-row {
    flex-direction: column;
  }

  .stats {
    flex-direction: column;
  }

  .stat {
    margin-bottom: 1em;
  }

  .reverse-stack {
    flex-direction: column-reverse;
  }
}

#contact {
  background-image: url("https://res.cloudinary.com/ajhtoo/image/upload/v1515176156/envelope-icon_dxf4fo.svg");
  background-repeat: no-repeat;
  background-position-x: left;
  background-position-y: center;
  background-color: orange;
  border: none;
  border-radius: 3px 0 0 3px;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, .3);
  position: fixed;
  padding: 1rem 2.5rem 1rem 1rem;
  z-index: 3;
  width: 42px;
  height: 28px;
  top: 50%;
  cursor: pointer;
  display: flex;
  align-self: right;
}

</style>
