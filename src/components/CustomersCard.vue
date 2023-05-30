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
  </div>
</template>

<style lang="scss" scoped>
.custom-card {
  width: calc((100% - 3rem) / 4);
  text-align: center;
}
</style>
