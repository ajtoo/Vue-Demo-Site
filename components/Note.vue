<template>
    <figure class="note" v-observe-visibility="visibilityChanged" v-bind:class="{'fade-in': visible}">
        <img class="note-icon" src="https://res.cloudinary.com/ajhtoo/image/upload/c_scale,w_26/v1515176158/Vue%20Demo%20Site/page-icon_f6kpd2.svg"/>
        <p><slot>Lorem ipsum dolor sit amet, ac dis arcu libero, pulvinar vitae lectus cursus</slot></p>
    </figure>
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
  },
  mounted: function () {
    this.visible = true
  }
}
</script>

<style scoped>
  .note {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 30vw;
    text-align: left;
  }
  .note-icon {
    margin-right: .75em;
    max-width: 26px;
  }

  @media (max-width: 768px) {
    .note {
      width: 80vw;
    }
  }
</style>
