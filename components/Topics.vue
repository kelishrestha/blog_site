<template>
  <div>
    <div class="container-fluid bg-light">
      <div class="series-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
        <h1 class="display-5 text-uppercase">Creations</h1>
        <p class="lead">
          <small>
            The current YOU is the best version of yourself.
          </small>
        </p>
      </div>
    </div>
    <div class="d-md-flex flex-md-equal w-100">
      <div class="bg-dark pt-3 px-3 pt-md-5 px-md-5 text-center text-white overflow-hidden">
        <div class="my-3 py-3">
          <h2 class="display-5">
            <a href="/the-peach-fall" class="comfortaa">
            <strong>
            The Peach Fall
            </strong>
            </a>
          </h2>
          <p class="lead mb-0 comfortaa">Mini-series.</p>
        </div>
        <div class="bg-light shadow-sm mx-auto my-4 topic-bg text-dark p-4">
          <p class="lead">
            <h2 class="topic-tagline">
              How will you get up again when you descend into the peach fall?
            </h2>
            <a href="/the-peach-fall" class="btn btn-danger p-3">
              <div class="icon-book-open"></div>
              <span class="series-header"> Read Now</span>
            </a>
          </p>
        </div>
      </div>
      <div class="bg-danger pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden text-light">
        <div class="my-3 p-3">
          <h2 class="display-5">
            <a href="/the-sore-transition" class="comfortaa">
            <strong>
              The Sore Transition
            </strong>
            </a>
          </h2>
          <p class="lead mb-0 comfortaa">Poetic Collection.</p>
        </div>
        <div class="bg-dark shadow-sm mx-auto my-4 topic-bg p-4">
          <p class="lead">
            <h2 class="topic-tagline">
              I take an oath to slowly become the one I ought to be...
            </h2>
            <a href="/the-sore-transition" class="btn btn-danger p-3">
              <div class="icon-book-open"></div>
              <span class="series-header"> Read Now</span>
            </a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .series-header {
    max-width: 700px;
    font-family: 'Comfortaa', sans-serif;
  }

  .topic-tagline {
    margin: 2% 20%;
    height: 5em;
    font-family: 'Caveat', sans-serif;
  }
  /*
 * Extra utilities
 */

  .flex-equal>* {
    -ms-flex: 1;
    flex: 1;
  }

  @media (min-width: 768px) {
    .flex-md-equal>* {
      -ms-flex: 1;
      flex: 1;
    }
  }

  .overflow-hidden {
    overflow: hidden;
  }

  .topic-bg {
    width: 80%;
    height: 300px;
    border-radius: 21px;
  }

  a {
    color: #fff;
  }
  a:focus,
  a:hover {
    color: rgb(254, 176, 176);
    text-decoration: none;
  }


</style>
