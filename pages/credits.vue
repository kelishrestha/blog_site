<template>
  <div>
    <Navbar />
    <div class="container-fluid bg-white footer-bottom-margin">
      <div class="series-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
        <h4 class="display-4 text-center rock-salt text-danger"><u>Credits</u></h4>
        <p class="lead d-none">
          <small>
            The current YOU is the best version of yourself.
          </small>
        </p>
      </div>
      <div class="container my-4">
        <div class="card-columns">
          <div class="card" v-for="photoCredit in photoCredits">
            <ul class="list-group list-group-flush">
              <li class="list-group-item">
                <div class="media">
                  <img v-bind:src="photoCredit.imageUrl" class="media-image mr-3" alt="">
                  <div class="media-body comfortaa">Source: {{ photoCredit.source }}<p v-html="photoCredit.title"></p></div>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'

import credits from '../assets/data/credits.json'

export default {
  components: {
    Navbar,
    Footer
  },
  data() {
    var imageCredits = credits.photo;
    return {
      photoCredits: imageCredits,
      title: 'Credits'
    }
  },
  head () {
    return {
      title: this.title,
      // meta: [
      //   // hid is used as unique identifier. Do not use `vmid` for it as it will not work
      //   { hid: 'description', name: 'description', content: 'My custom description' }
      // ]
    }
  }
}
</script>

<style scoped>
  .series-header {
    max-width: 700px;
    font-family: 'Comfortaa', sans-serif;
  }
  .media-image {
    width: 64px;
    height: 64px;
  }
  .footer-bottom-margin{
    margin-bottom: 11.4em;
  }
</style>
