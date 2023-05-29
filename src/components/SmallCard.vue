<script>
export default {
  props: {
    urlImg: String,
    carType: String,
  },
};
</script>
<template>
  <div class="card">
    <img :src="urlImg" alt="" />
    <p>{{ carType }}</p>
    <p>2 listings</p>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: calc(100% / 6);
}
</style>
