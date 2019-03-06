<template>
  <section class="angled-banner">
    <p class="angled-banner-content">
      <slot>
        Lorem ipsum dolor sit amet, ac dis arcu libero, pulvinar vitae lectus curses. Purus libero amet, at dui, tincidunt nunc vestibulum in justo, a faucibus ipsum hendrerit semper ipsem ac.
      </slot>
    </p>
  </section>
</template>

<style scoped>
  .angled-banner {
    background-image: url("https://res.cloudinary.com/ajhtoo/image/upload/v1515176158/Vue%20Demo%20Site/slanted-gradient-background_kgru5b.svg");
    background-repeat: no-repeat;
    background-position-x: center;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    padding: 5em 3em 2em;
  }
  
  .angled-banner-content {
    font-size: 1.5em;
    color: white;
    width: 60vw;
  }

  @media (max-width: 768px) {
    .angled-banner-content {
      font-size: 1.15em;
    }
  }
</style>