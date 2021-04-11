<template>
  <div id="app">
    <aboutme></aboutme>
    <router-view/>
  </div>
</template>

<script>
import aboutme from "./views/Aboutme";

export default {
  components: {aboutme,}
}
</script>
<style>
#app {
  background-color:#6E8B3D;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
