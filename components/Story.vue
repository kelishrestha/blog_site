<template>
  <div>
    <main role="main" class="container pt-5">
      <section class="wrapper row">
        <ul class="breadCrumbs">
          <li>
            <a href="/" title="Home" class="animation">
              <div class="icon-home icon-padding"></div>
            </a>
          </li>
          <li><a v-bind:href="parentPath" title="Home" class="animation text-capitalize">{{ $nuxt.$route.params.topic.replace(/-/gi, " ") }}</a></li>
          <li class= "activePage"><p v-bind:title="$nuxt.$route.params.story.replace(/-/gi, ' ')" class="animation text-capitalize">{{ $nuxt.$route.params.story.replace(/-/gi, " ") }}</p></li>
          <div class="clear"></div>
        </ul>
      </section>
      <div class="starter-template row">
        <div class="col">
          <div class="card shadow-lg">
            <div class="card-body">
              <h5 class="card-title mb-0">{{ title }}</h5>
              <small class="card-subtitle mb-2 text-muted">{{ publishedDate }}</small>
              <h6>
                <b-badge variant="danger" v-for="labelTag in labels" class="mr-1">{{ labelTag }}</b-badge>
              </h6>
              <p class="card-text pt-4">
                <pre>{{ content }}</pre>
                <footer class="blockquote-footer float-right">
                  <em>
                    Shizenluver
                  </em>
                </footer>
              </p>
            </div>
          </div>
        </div>
        <div class="col col-4 mx-3">
          <div class="card shadow bg-archive text-white">
            <div class="card-body">
              <h5 class="card-title comfortaa">Archives</h5>
              <h6 class="card-subtitle my-2">
                <a href="/the-peach-fall" class="card-link archive-link">The Peach Fall</a>
              </h6>
              <h6 class="card-subtitle my-2">
                <a href="/the-sore-transition" class="card-link archive-link">The Sore Transition</a>
              </h6>
            </div>
          </div>
        </div>
      </div>

    </main><!-- /.container -->
  </div>
</template>

<script>
import topicDetails from '../assets/data/topic-details.json'

export default {
  data ({ params }) {
    var currentTopic = this.$route.params.topic;
    var currentPath = this.$route.path;
    let content, title, publishedDate, labels;
    var allTopics = topicDetails.topics;
    allTopics.forEach(topic => {
      if (topic.routeName == currentTopic){
        var stories = topic.stories;
        stories.forEach(story => {
          if (story.routeName == currentPath){
            content = story.content;
            title = story.name;
            publishedDate = story.publishedDate;
            labels = story.labels;
          }
        });
      };
    });
    return {
      content: content.join('').replace(/<br\s*[\/]?>/gi, "\n"),
      parentPath: '/' + this.$route.params.topic,
      title: title,
      publishedDate: publishedDate,
      labels: labels
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
  .starter-template {
    padding: 1rem 1.5rem;
  }
  pre {
    /* font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji"; */
    font-family: 'Mali', sans-serif;
    font-size: 16px;
  }

  .icon-padding {
    padding: 0.75em;
  }

  .archive-link{
    color: #ff5757;;
  }

  .bg-archive {
    background-image: url('https://images.unsplash.com/photo-1518289646039-3e6c87a5aaf6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1951&q=80');
  }
</style>
