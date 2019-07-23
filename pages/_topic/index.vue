<template>
  <div>
    <Navbar />
    <TopicStory />
    <Footer />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import TopicStory from '~/components/TopicStory.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Navbar,
    TopicStory,
    Footer
  },
  watchQuery: ['topic'],
  asyncData ({ params }) {
    const topic = params.topic // When calling /abc the topic will be "abc"
    console.log(topic);
    return { topic }
  }
}
</script>
