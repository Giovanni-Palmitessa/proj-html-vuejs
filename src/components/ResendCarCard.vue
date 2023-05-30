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
    <p>06.07.2022 - Auto Car</p>
    <h3>{{ brand }}</h3>
    <p class="article">{{ article }}</p>
    <div class="btn">More</div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;
.resendCard {
  width: calc((100% - 9rem) / 4);
  padding: 1rem;
  border: 1px solid $gray-main;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 6rem;
  img {
    width: 100%;
  }
  h3 {
    margin: 1rem 0;
    font-size: 1.4rem;
  }
  .article {
    text-align: start;
    font-size: 0.9rem;
    color: $gray-main;
  }
  .btn {
    width: 150px;
    color: $white-main;
    font-weight: 700;
    text-align: center;
    background-color: $black-main;
    padding: 1.5rem 2rem;
    margin-top: 2rem;
    &:hover {
      cursor: pointer;
    }
  }
}
</style>
