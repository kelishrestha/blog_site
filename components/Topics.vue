<template>
  <div>
    <div class="container-fluid bg-light">
      <div class="series-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
        <h1 class="display-4">Series</h1>
        <p class="lead">Some tagline.</p>
      </div>
    </div>
    <div class="d-md-flex flex-md-equal w-100">
      <div class="bg-dark pt-3 px-3 pt-md-5 px-md-5 text-center text-white overflow-hidden">
        <div class="my-3 py-3">
          <h2 class="display-5">
            <a href="/the-peach-fall">
            The Peach Fall
            </a>
          </h2>
          <p class="lead mb-0">Mini-series.</p>
        </div>
        <div class="bg-light shadow-sm mx-auto my-4 topic-bg text-dark p-4">
          <p class="lead">Some tagline.</p>
        </div>
      </div>
      <div class="bg-danger pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden text-light">
        <div class="my-3 p-3">
          <h2 class="display-5">
            <a href="/the-sore-transition">
              The Sore Transition
            </a>
          </h2>
          <p class="lead mb-0">Poetic Collection.</p>
        </div>
        <div class="bg-dark shadow-sm mx-auto my-4 topic-bg p-4">
          <p class="lead">Some tagline</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .series-header {
    max-width: 700px;
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
