<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <!-- <router-link to="/users">User</router-link> | -->
    <router-link to="/attend">Attend</router-link> |
    <router-link to="/per">Per</router-link> |

  </nav>
  <router-view/>
</template>

<script>
export default { 
  mounted() {
    this.$store.dispatch('getUsers')
  }
}

</script>





<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
