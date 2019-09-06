<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <a href="">About</a>
    <router-view/>
  </div>
</template>

<script>
/*
created () {
console.log('route', this.$route.path)
this.$router.replace(this.$route.query.redirect || '/')
}
this.$router.replace(this.$route.fullPath || '/')
*/
export default {
  name: 'App',
  created () {
    // console.log('route', this.$route.path)
    // this.$router.replace(this.$route.query.redirect || '/')
    console.log('route', this.$route.fullPath)
    this.$router.replace(this.$route.fullPath || '/')
  }
}
</script>
<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
