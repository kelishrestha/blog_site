<template>
  <div>
    <Navbar />
    <div class="container my-5">
      <h4 class="display-4 text-center rock-salt text-danger"><u>My Archives</u></h4>
      <div v-for="topic in topics" class="my-4 p-4 border rounded">
        <h2 class="display-5 text-center permanent-marker mb-4">{{ topic.name }}</h2>
        <div class="card-columns">
          <div class="card bg-dark text-white text-center border-0 shadow" v-for="story in topic.stories">
            <img v-bind:src="story.backgroundImage" class="card-img card-img-style" alt="Image">
            <div class="card-img-overlay my-5">
              <h5 class="card-title comfortaa">{{ story.name }}</h5>
              <p class="card-text comfortaa">{{ story.publishedDate }}</p>
              <div class="btn-group">
                <a v-bind:href="story.routeName" class="btn btn-sm btn-danger comfortaa">View</a>
              </div>
            </div>
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

import topicDetails from '../assets/data/topic-details.json'

export default {
  components: {
    Navbar,
    Footer
  },
  data () {
    return {
      topics: topicDetails.topics,
      title: 'Shizenluver | Archives'
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
.card-img-style {
  opacity: 0.5;
}
</style>

