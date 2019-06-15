<template>
  <div>
    <main role="main" class="container pt-5">
      <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
          <li class="breadcrumb-item text-capitalize"><a href="#" class="text-danger">{{ $nuxt.$route.params.topic.replace(/-/gi, " ") }}</a></li>
          <li class="breadcrumb-item text-capitalize active" aria-current="page">{{ $nuxt.$route.params.story.replace(/-/gi, " ") }}</li>
        </ol>
      </nav>
      <div class="starter-template row">
        <div class="col">
          <div class="card">
            <div class="card-body">
              <h5 class="card-title mb-0">The Healer</h5>
              <small class="card-subtitle mb-2 text-muted">Thursday, January 17, 2019</small>
              <p class="card-text pt-4">
                <pre>
Dark pale nights, those unknown chilling voices
Thrusting into my head, locked down, I fall down
Casted upon a spell
I tried to break them apart but nothing would gain

Every day it was the same
Fears and doubts pilling up against
The cold chill inside my heart
The concussion over my head
Never ending in a blissful state

I was broken when I heard a soulful song
Healing me red through my blue veins
Scattering those ultrasonic sounds into seven waves
Forged with its painful stories that even destroyed vain

The melody pierced through my skin
Charging me up with its troth
For it was only meant for me
To heal myself and comfort me with its warm soul

Every time I suffocated, I found you as my escape
Antidoting me with your words inside my veins
I held my head high with your comforts again
I shall might rise up in this world of pain

You are my healer
You are my fiend
Will you heal me whenever I ask you not to save me?
Will you set me free whenever I push you off to leave me alone?

I close my eyes and feel you grin
Only to know that you are not real
I save myself in your world where you seal
The broken me inside your black shining wings
                </pre>
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
          <div class="card bg-dark text-white">
            <div class="card-body">
              <h5 class="card-title">Archives</h5>
              <h6 class="card-subtitle my-2">
                <a href="/the-peach-fall" class="card-link text-danger">The Peach Fall</a>
              </h6>
              <h6 class="card-subtitle my-2">
                <a href="/the-sore-transition" class="card-link text-danger">The Sore Transition</a>
              </h6>
            </div>
          </div>
        </div>
      </div>

    </main><!-- /.container -->
  </div>
</template>

<style scoped>
  .starter-template {
    padding: 1rem 1.5rem;
  }
  pre {
    /* font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji"; */
    font-family: 'Mali', sans-serif;
    font-size: 16px;
  }
</style>
