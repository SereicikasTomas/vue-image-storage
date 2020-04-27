<template>
  <div>Image<Logo class="logo" />Storage</div>
</template>

<script>
import Logo from "../assets/file-archive-solid.svg";

export default {
  name: "AppHeader",
  components: {
    Logo
  }
};
</script>

<style lang="scss" scoped>
.logo {
  height: 20px;
  color: lightblue;
}
</style>
