<script>
export default {
  props: {
    imgUrl: String,
    name: String,
    type: String,
    price: String,
    brand: String,
    fuel: String,
  },
};
</script>
<template>
  <div class="bigCard">
    <img :src="imgUrl" :alt="name" />
    <p>
      {{ name }}
      <font-awesome-icon icon="fa-solid fa-circle-check" class="icon" />
    </p>
    <p class="carType">{{ type }}</p>
    <div class="shop">
      <p>
        <font-awesome-icon icon="fa-solid fa-dollar-sign" class="icon" />
        {{ price }}
      </p>
      <p>
        <font-awesome-icon icon="fa-solid fa-car" class="icon" /> {{ brand }}
      </p>
      <p>
        <font-awesome-icon icon="fa-solid fa-gas-pump" class="icon" />
        {{ fuel }}
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;
.bigCard {
  width: calc(100% / 4);
  padding: 0.5rem;
  margin-bottom: 1rem;
  box-shadow: 1px 1px 5px rgba(199, 189, 189, 0.403);
  &:hover {
    cursor: pointer;
  }
  img {
    width: 100%;
    margin-bottom: 8px;
  }
  .carType {
    font-size: 0.8rem;
    margin-top: 8px;
  }
  .shop {
    display: flex;
    gap: 0.5rem;
    font-size: 0.8rem;
    margin-top: 8px;
    .icon {
      width: 10px;
    }
  }
}
</style>
