<template>
  <div>
    <AppHeader></AppHeader>
    <div class="view">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader";

export default {
  name: "App",
  components: {
    AppHeader
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
  font-family: Arial, Helvetica, sans-serif;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
  color: black;
}

.view {
  margin: 5%;
}
</style>
