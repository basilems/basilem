<template>
  <nav class="bg-gradient-to-b from-orange-600 to-gray-700 flex items-center">
    <div class="w-full max-w-sm justify-self-center">
      <img src="@/assets/BM.png" class="md:h-full md:w-48 object-cover">
    </div>
    <div class="w-full flex">
      <router-link to="/" class="flex-auto rounded-lg">Home</router-link>
      <router-link to="/about" class="flex-auto rounded-lg">About</router-link>
      <router-link to="/who" class="flex-auto rounded-lg">Who am I</router-link>
    </div>
  </nav>
  <router-view/>
</template>

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
