<template>
  <div class="header">
    <a href="/" class="logo">
      Im<ImageIcon class="icon" />ge Stor<ArchiveIcon class="icon" />ge
    </a>
    <nav>
      <ul>
        <li v-if="isLoggedIn" @click="login">
          <a href="#">
            Logout
          </a>
        </li>
        <li v-else @click="login">
          <a href="#">
            Login
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
import ArchiveIcon from "../assets/file-archive-regular.svg";
import ImageIcon from "../assets/file-image-regular.svg";
import { mapActions, mapGetters } from "vuex";

export default {
  name: "AppHeader",
  components: {
    ArchiveIcon,
    ImageIcon
  },
  methods: mapActions(["login"]),
  computed: mapGetters(["isLoggedIn"])
};
</script>

<style lang="scss" scoped>
.header {
  border-bottom: 1px solid black;
  min-height: 10vh;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 3rem 5%;
}
.logo {
  display: flex;
  align-items: center;
  font-size: 3rem;
  color: rgb(77, 170, 201);
  text-decoration: none;
}
.icon {
  height: 2rem;
  color: rgb(77, 170, 201);
  margin: 0 0.2rem;
}

nav {
  font-size: 2rem;
  a {
    color: rgb(77, 170, 201);
  }
}
</style>
