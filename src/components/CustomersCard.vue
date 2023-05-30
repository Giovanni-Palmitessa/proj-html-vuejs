<script>
export default {
  props: {
    comment: String,
    image: String,
    name: String,
  },
};
</script>
<template>
  <div class="custom-card">
    <p>{{ comment }}</p>
    <img :src="image" :alt="name" />
    <p>{{ name }}</p>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;
.custom-card {
  width: calc((100% - 3rem) / 4);
  padding: 1rem;
  text-align: center;
  background-color: $white-main;
  border-radius: 15px;
  img {
    width: 30%;
  }
}
</style>
