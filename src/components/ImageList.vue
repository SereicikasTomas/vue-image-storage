<template>
  <div>
    <div v-if="isLoggedIn" class="image-container">
      <img v-for="image in allImages" :key="image.id" :src="image.link" />
    </div>
    <h2 v-else>Log in to get started.</h2>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: "ImageList",
  computed: mapGetters(["allImages", "isLoggedIn"]),
  methods: mapActions(["fetchImages"]),
  created() {
    this.fetchImages();
  }
};
</script>

<style lang="scss" scoped>
.image-container {
  column-count: 3;
  column-gap: 2rem;

  img {
    width: 100%;
    margin-bottom: 2rem;
    border-radius: 5px;
  }
}

h2 {
  color: rgb(77, 170, 201);
  font-size: 3rem;
  font-weight: 300;
  text-align: center;
}
</style>
