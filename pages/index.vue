<template>
  <div>
    <Cover />
    <Topics />
    <Footer />
  </div>
</template>

<script>
import Cover from '~/components/Cover.vue'
import Topics from '~/components/Topics.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Cover,
    Topics,
    Footer
  },
  data() {
    return {
      title: 'Shizenluver The Blog'
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
