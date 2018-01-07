<template>
    <figure class="note">
        <img class="note-icon" src="https://res.cloudinary.com/ajhtoo/image/upload/v1515176158/page-icon_f6kpd2.svg"/>
        <p>Lorem ipsum dolor sit amet, ac dis arcu libero, pulvinar vitae lectus cursus</p>
    </figure>
</template>

<style>
  .note {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    width: 30vw;
    text-align: left;
  }
  .note-icon {
    margin: .75em;
  }

  @media (max-width: 768px) {
    .note {
      width: 80vw;
    }
  }
</style>
