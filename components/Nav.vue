<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light mb-5">
    <a class="navbar-brand" href="#">Nuxt App</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active pr-3" >
          <nuxt-link to="/">Home </nuxt-link>
        </li>
        <li class="nav-item pr-3">
          <nuxt-link to="/users">Users </nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link to="/posts">Posts </nuxt-link>
        </li>
      </ul>
    </div>
  </nav>

</template>
