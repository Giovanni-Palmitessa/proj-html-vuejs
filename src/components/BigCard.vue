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
    <img
      src="../assets/img/bmw-8-series-convertible-technical-data-sp-desktop-400x300.jpg"
      alt=""
    />
    <p>
      BMW M9 <font-awesome-icon icon="fa-solid fa-circle-check" class="icon" />
    </p>
    <p class="carType">Cabrio</p>
    <div class="shop">
      <p>
        <font-awesome-icon icon="fa-solid fa-dollar-sign" class="icon" /> 34000
      </p>
      <p><font-awesome-icon icon="fa-solid fa-car" class="icon" /> BMW</p>
      <p>
        <font-awesome-icon icon="fa-solid fa-gas-pump" class="icon" /> Electric
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.bigCard {
  width: calc(100% / 4);
  padding: 0.5rem;
  border: 1px solid gray;
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
