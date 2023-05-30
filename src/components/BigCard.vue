<script>
export default {};
</script>
<template>
  <div class="bigCard">
    <img
      src="../assets/img/bmw-8-series-convertible-technical-data-sp-desktop-400x300.jpg"
      alt=""
    />
    <p>BMW M9 <font-awesome-icon icon="fa-solid fa-circle-check" /></p>
    <p>Cabrio</p>
    <div class="shop">
      <p><font-awesome-icon icon="fa-solid fa-dollar-sign" /> 34000</p>
      <p><font-awesome-icon icon="fa-solid fa-car" /> BMW</p>
      <p><font-awesome-icon icon="fa-solid fa-gas-pump" /> Electric</p>
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
  }
}
</style>
