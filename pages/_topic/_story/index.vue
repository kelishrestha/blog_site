<template>
  <div>
    <Navbar />
    <Story />
    <Footer />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import Story from '~/components/Story.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Navbar,
    Story,
    Footer
  }
}
</script>
