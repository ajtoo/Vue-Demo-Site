<template>
  <header class="headline-cta">
    <h1 class="headline">Lorem Ipsum Lorem Ipsum</h1>
    <button class="cta">Button</button>
  </header>
</template>

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
    background: linear-gradient(90deg,#f76b1c,#f3b160);
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