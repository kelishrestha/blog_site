<template>
  <div>
    <main role="main">

      <section class="jumbotron text-center bg-light rounded-0">
        <div class="container">
          <h1 class="jumbotron-heading text-capitalize cover-text text-danger">{{ topic.name }}</h1>
          <p class="lead cover-heading">{{ topic.tagline }}</p>
          <p class="d-none">
            <a href="#" class="btn btn-primary my-2">Main call to action</a>
            <a href="#" class="btn btn-secondary my-2">Secondary action</a>
          </p>
        </div>
      </section>

      <div class="album py-5 topic-list-bg">
        <div class="container">
          <div class="row">
            <div class="col-md-4" v-for="story in topic.stories">
              <div class="card border-0 mb-4 shadow-lg text-white bg-danger">
                <img v-bind:src="story.backgroundImage" alt="" class="bd-placeholder-img card-img-top">
                <div class="card-body">
                  <div class="d-flex justify-content-between align-items-center">
                    <div class="card-title">
                      <h4 class="mb-0">
                        {{ story.name }}
                      </h4>
                      <small>{{ story.publishedDate }}</small>
                    </div>
                    <div class="btn-group">
                      <a v-bind:href="story.routeName" class="btn btn-sm btn-dark">View</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

    </main>
  </div>
</template>

<script>
import topicDetails from '../assets/data/topic-details.json'

export default {
  data ({ params }) {
    var currentTopic = this.$route.params.topic;
    var topic;
    var allTopics = topicDetails.topics;
    allTopics.forEach(element => {
      if (element.routeName == currentTopic){
        topic = element;
      };
    });
    console.log(topic)
    return {
      topics: topicDetails,
      topic: topic
    }
  }
}
</script>

<style scoped>
  .bd-placeholder-img {
    font-size: 1.125rem;
    text-anchor: middle;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  @media (min-width: 768px) {
    .bd-placeholder-img-lg {
      font-size: 3.5rem;
    }
  }

  .jumbotron {
    padding-top: 3rem;
    padding-bottom: 3rem;
    margin-bottom: 0;
    background-color: #fff;
  }

  @media (min-width: 768px) {
    .jumbotron {
      padding-top: 6rem;
      padding-bottom: 6rem;
    }
  }

  .jumbotron p:last-child {
    margin-bottom: 0;
  }

  .jumbotron-heading {
    font-weight: 300;
  }

  .jumbotron .container {
    max-width: 40rem;
  }

  footer {
    padding-top: 3rem;
    padding-bottom: 3rem;
  }

  footer p {
    margin-bottom: .25rem;
  }

  .topic-bg{
    /* background-image: url('https://images.unsplash.com/photo-1529641484336-ef35148bab06?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80'); */
    background: url('https://images.unsplash.com/photo-1505562130589-9879683e72da?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1650&q=80');
    /* background-position: bottom */

  }

  .topic-list-bg{
    /* background-image: url('https://images.unsplash.com/photo-1529641484336-ef35148bab06?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80'); */
    background: url('https://images.unsplash.com/photo-1505562130589-9879683e72da?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1650&q=80');
    background-size: cover;
    /* background-position: bottom */
  }

  .cover-heading {
    font-family: 'Permanent Marker', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  .cover-text {
    font-family: 'Rock Salt', cursive;
  }
</style>
