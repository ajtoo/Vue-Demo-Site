<template>
  <p class="animated-number" v-observe-visibility="visibilityChanged">{{this.displayNumber}}%</p>
</template>

<script>
  export default {
    props: {'number': {default: 0}, 'duration': {default: 1000}},
    data: function () {
      return {
        displayNumber: 0,
        counting: false
      }
    },
    methods: {
      count () {
        this.counting = true
        const self = this
        const range = this.number - this.displayNumber
        const increment = this.number > this.displayNumber ? 1 : -1
        const interval = Math.abs(Math.floor(this.duration / range))
        const timer = setInterval(function () {
          self.displayNumber += increment
          if (self.displayNumber === self.number) {
            self.counting = false
            clearInterval(timer)
          }
        }, interval)
      },
      visibilityChanged (isVisible, entry) {
        if (!this.counting) {
          this.displayNumber = 0
          this.count()
        }
      }
    },
    mounted: function () {
      // this.count()
    }
  }
</script>

<style scoped>
  .animated-number {
    font-size: 3em;
    font-weight: bold;
  }
</style>


