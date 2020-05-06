<template>
  <div>
    <input type="file" />
    <span>Drag files here to upload an image.</span>
  </div>
</template>

<script>
export default {
  name: "UploadForm"
};
</script>

<style lang="scss" scoped>
div {
  height: 30vh;
  border: 2px dashed black;
  border-radius: 5px;
  display: flex;
  position: relative;
  display: flex;
  transition: background-color 300ms ease;
  &:hover {
    background-color: #eee;
  }

  input {
    position: absolute;
    width: 100%;
    height: 30vh;
    opacity: 0;
  }

  span {
    font-size: 2rem;
    margin: auto;
  }
}
</style>
