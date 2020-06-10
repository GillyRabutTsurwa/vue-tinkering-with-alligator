<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <div class="nav">
      <router-link to="/gator">Gator</router-link>
      <router-link to="/swamp">Swamp</router-link>
    </div>
    <hr />
    <div class="router-view">
      <transition name="slither">
        <router-view></router-view>
      </transition>
    </div>
  </div>
</template>

<script>
// import Gator from "./components/Gator";
// import Swamp from "./components/Swamp";

export default {
  name: "App",
  components: {
    // Gator: Gator,
    // Swamp: Swamp
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.slither-enter-active,
.slither-leave-active {
  /* transition: transform 1s; */
  transition: opacity 1s;
  position: relative;
}

.slither-enter,
.slither-leave-to {
  /* transform: translateX(-100%); */
  opacity: 0;
}

.slither-enter-to,
.slither-leave {
  /* transform: translateX(0); */
  opacity: 1;
}

/* NOTE: This works in styling the router-link element because it renders to an a tag at the end */
a {
  margin: 1em;
}

h1 {
  position: fixed;
}
</style>
