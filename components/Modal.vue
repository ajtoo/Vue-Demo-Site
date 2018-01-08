<template>

  <transition name="modal">
    <div class="modal-mask" @click="$emit('close')">
      <div class="modal-wrapper">
        <div class="modal-container" @click.stop>
          <div class="modal-header">
            <h4 class="medium-orange-text">
              Lorem Ipsum
            </h4>
          </div>

          <div class="modal-body">
            <form id="email-form">
              <label for="name">Your Name</label>
              <input class="name-input" name="name" v-model="name"/>
              <section>
                <div class="short-input">
                  <label for="email">Your Email</label>
                  <input class="email-input" name="email"  v-model="email"/>
                </div>
                <div class="short-input">
                  <label for="phone">Phone Number</label>
                  <input class="phone-input" name="phone"  v-model="phone"/>
                </div>
              </section>
              <label for="message">Message</label>
              <textarea class="message-input" name="message"  v-model="message"/>
            </form>
          </div>

          <div class="modal-footer">
            <button class="cta" @click="openEmailClient">Button</button>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
  export default {
    methods: {
      openEmailClient () {
        console.log(this.message)
        window.location.href = 'mailto:username@example.com'
      }
    }
  }
</script>

<style>
  .modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, .5);
    display: table;
    transition: opacity .3s ease;
  }

  .modal-wrapper {
    display: table-cell;
    vertical-align: middle;
  }

  .modal-container {
    width: 30vw;
    margin: 0px auto;
    padding: 20px 30px;
    transition: all .3s ease;
    font-family: Helvetica, Arial, sans-serif;
  }

  .modal-header h3 {
    margin-top: 0;
    color: #42b983;
  }

  .modal-body {
    margin: 20px 0;
  }

  .modal-default-button {
    float: right;
  }

  /*
  * The following styles are auto-applied to elements with
  * transition="modal" when their visibility is toggled
  * by Vue.js.
  *
  * You can easily play with the modal transition by editing
  * these styles.
  */

  .modal-enter {
    opacity: 0;
  }

  .modal-leave-active {
    opacity: 0;
  }

  .modal-enter .modal-container,
  .modal-leave-active .modal-container {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }

  #email-form {
    display: flex;
    flex-direction: column;
    color: white;
    text-align: left;
  }

  #email-form input, textarea {
    border-radius: 3px;
    border: none;
    padding: .5rem .5rem;
  }

  #email-form section {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: 1rem 0;
  }

  .message-input {
    height: 7rem;
  }

  .short-input {
    display: flex;
    flex-direction: column;
  }
</style>
