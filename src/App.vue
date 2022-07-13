<template>
  <nav class="bg-gradient-to-b from-orange-600 to-gray-100 dark:to-gray-700 flex items-center justify-between">
    <div class="w-full max-w-sm self-end grow">
      <img src="@/assets/BM.svg" class="h-full w-12 sm:w-32">
    </div>
    <div class="hidden"></div>
    <div class="w-full grid grid-cols-3 justify-end grow-0">
      <router-link to="/" class="rounded-lg">Home</router-link>
      <router-link to="/who" class="rounded-lg">Who am I</router-link>
      <router-link to="/about" class="rounded-lg">About</router-link>
    </div>

  </nav>
  <div class="">
    <router-view/>
  </div>
  <footer class="self-end">
    This is a fotter
  </footer>
</template>

<script setup>
// On page load or when changing themes, best to add inline in `head` to avoid FOUC
if (localStorage.getItem('color-theme') === 'dark' || (!('color-theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
  document.documentElement.classList.add('dark')
} else {
  document.documentElement.classList.remove('dark')
}
</script>

<style lang="scss">
body{
  background-color: rgb(51 65 85);
  color: rgb(255, 255, 255)
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  // color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: rgb(221, 227, 235);

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
