<script>
export default {
  props: {
    img: String,
    brand: String,
    article: String,
  },
};
</script>
<template>
  <div class="resendCard">
    <img :src="img" :alt="brand" />
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;
.resendCard {
  width: calc((100% - 6rem) / 4);
  padding: 1rem;
  border: 1px solid $gray-main;
  border-radius: 10px;
  img {
    width: 100%;
  }
}
</style>
