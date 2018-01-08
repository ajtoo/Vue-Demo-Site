<template>
  <header class="headline-cta">
    <h1 class="headline">Lorem Ipsum Lorem Ipsum</h1>
    <button class="cta" @click="buttonClicked">Button</button>
  </header>
</template>

<script>
  export default {
    methods: {
      buttonClicked () {
        alert('fill in your button click function here')
      }
    }
  }
</script>

<style>
  .headline-cta {
    display: flex;
    flex-direction: column;
    align-items: start;
    position: relative;
    top: -12rem;
    width: 100%;
    max-width: 1355px;
    margin-left: 20%;
    margin-bottom: -6rem;
  }

  .headline {
    position: relative;
    font-size: 2.75rem;
    color: white;
    text-align: left;
    display: inline-block;
  }

  .cta {
    margin-top: 1rem;
    font-size: 1.15rem;
    background: linear-gradient(90deg,#f36819,#f7931d);
    border-radius: 5px;
    border: none;
    box-shadow: 1px 1px 2px rgba(0, 0, 0, .2);
    color: white;
    padding: .4em 4em;
    cursor: pointer;
  }

  @media (max-width: 576px) {
    .headline-cta {
      top: -14rem;
    }
  }
</style>