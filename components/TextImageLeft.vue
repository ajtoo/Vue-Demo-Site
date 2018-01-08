<template>
  <section class="content-row spacing-below" v-observe-visibility="visibilityChanged" v-bind:class="{'fade-in': visible}">
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
</template>

<script>
export default {
  data: function () {
    return {
      visible: false
    }
  },
  methods: {
    visibilityChanged (isVisible, entry) {
      this.visible = isVisible
    }
  }
}
</script>