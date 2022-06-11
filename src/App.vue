<template>
  <nav class="bg-gradient-to-b from-orange-600 to-gray-700 flex flex-row flex-nowrap ">
    <router-link to="/" class="flex-1 rounded-lg">Home</router-link>
    <router-link to="/about" class="flex-1 rounded-lg">About</router-link>
    <router-link to="/who" class="flex-1 rounded-lg">Who am I</router-link>
  </nav>
  <router-view/>
</template>

<style lang="scss">
body{
  background-color: rgb(51 65 85);
  color: rgb(203 213 225)
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
    color: rgb(203 213 225);

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
