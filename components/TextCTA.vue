<template>
  <section class="content-row spacing-below" v-observe-visibility="visibilityChanged" v-bind:class="{'fade-in': visible}">
    <div class="sm-col-6">
      <p class="text-paragraph">
        <slot>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ellamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur
        </slot>
      </p>
    </div>
    <div class="sm-col-6">
      <button class="cta" @click="buttonClicked">Button</button>
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
