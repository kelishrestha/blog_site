<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark mb-0">
      <div class="container">
        <a class="navbar-brand w-25" href="/">
          <img src="../assets/logo.png" alt="" class="w-50">
        </a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSimple"
          aria-controls="navbarSimple" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSimple">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <a class="nav-link" href="/">Home <span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Archives</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Credits</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact</a>
            </li>
          </ul>
          <form class="form-inline my-2 my-md-0 d-none">
            <input class="form-control" type="text" placeholder="Search">
          </form>
        </div>

      </div>
    </nav>
  </div>
</template>

<style scoped>
body {
  padding-bottom: 20px;
}

.navbar {
  margin-bottom: 20px;
}
</style>
