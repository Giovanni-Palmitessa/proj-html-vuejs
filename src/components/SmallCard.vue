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
    <img :src="urlImg" :alt="carType" />
    <p class="type">{{ carType }}</p>
    <p class="listings">2 listings</p>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;
.card {
  width: calc(100% / 6);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  padding-bottom: 1.3rem;
  box-shadow: 1px 1px 5px rgba(199, 189, 189, 0.403);
  &:hover {
    cursor: pointer;
  }
  .type {
    font-size: 1.3rem;
  }
  .listings {
    font-size: 0.7rem;
    color: $gray-main;
  }
}
</style>
