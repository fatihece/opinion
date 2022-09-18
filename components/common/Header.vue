<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light border-0">
    <NuxtLink to="/" class="navbar-brand" tag="a">Koşe Yazısı</NuxtLink>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
        <NuxtLink to="/posts" class="nav-link" >Yazılar</NuxtLink>
      </ul>
      <ul class="navbar-nav my-2 my-lg-0">
        <NuxtLink to="/admin" class="nav-link" >Admin</NuxtLink>
      </ul>
    </div>
  </nav>
</template>
<style></style>
