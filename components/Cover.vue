<template>
  <div class="text-center full-page">
    <div class="cover-container d-flex w-100 h-100 p-3 mx-auto flex-column">
      <header class="masthead mb-auto">
        <div class="inner">
          <h3 class="masthead-brand w-50">
            <img src="~assets/logo.png" alt="Logo" class="w-50">
          </h3>
          <nav class="nav nav-masthead justify-content-center">
            <a class="nav-link active" href="/">Home</a>
            <a class="nav-link" href="/archives">Archives</a>
            <a class="nav-link" href="/credits">Credits</a>
            <a class="nav-link" href="#">Contact</a>
          </nav>
        </div>
      </header>
      <main role="main" class="inner cover">
        <h1 class="cover-heading">begin. again.</h1>
        <p class="lead cover-text">
          There's only one true path in life...
          <br>
          The road that leads to all...
          <br>
          Leads to one...
        </p>
      </main>

      <footer class="mastfoot mt-auto">
        <div class="inner d-none">
          <p>Shizenluver Blog</p>
        </div>
      </footer>
    </div>

  </div>
</template>

<style scoped>
/*
 * Globals
 */

/* Links */
a,
a:focus,
a:hover {
  color: #fff;
}

/* Custom default button */
.btn-secondary,
.btn-secondary:hover,
.btn-secondary:focus {
  color: #333;
  text-shadow: none; /* Prevent inheritance from `body` */
  background-color: #fff;
  border: .05rem solid #fff;
}


/*
 * Base structure
 */

.full-page {
  height: 100vh;
  /* background-color: #333; */
  background-image: url('https://images.unsplash.com/photo-1524721696987-b9527df9e512?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2690&q=80');
  display: -ms-flexbox;
  display: flex;
  color: #fff;
  box-shadow: inset 0 0 5rem rgba(55, 55, 55, 0.5);
}

.cover-container {
  max-width: 42em;
}

.cover-heading {
  font-family: 'Permanent Marker', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.cover-text {
  font-family: 'Rock Salt', cursive;
}

/*
 * Header
 */
.masthead {
  margin-bottom: 2rem;
}

.masthead-brand {
  margin-bottom: 0;
}

.nav-masthead .nav-link {
  padding: .25rem 0;
  font-weight: 700;
  color: rgba(255, 255, 255, .5);
  background-color: transparent;
  /* border-bottom: .25rem solid transparent; */
  font-family: 'Comfortaa', sans-serif;
}

.nav-masthead .nav-link:hover,
.nav-masthead .nav-link:focus {
  border-bottom-color: rgba(255, 255, 255, .25);
}

.nav-masthead .nav-link + .nav-link {
  margin-left: 1rem;
}

.nav-masthead .active {
  color: #fff;
  border-bottom-color: #fff;
}

@media (min-width: 48em) {
  .masthead-brand {
    float: left;
  }
  .nav-masthead {
    float: right;
  }
}


/*
 * Cover
 */
.cover {
  padding: 0 1.5rem;
}
.cover .btn-lg {
  padding: .75rem 1.25rem;
  font-weight: 700;
}


/*
 * Footer
 */
.mastfoot {
  color: rgba(255, 255, 255, .5);
}

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
</style>
