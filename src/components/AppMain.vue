<script>
export default {};
</script>
<template>
  <main>
    <section class="jumbo">
      <div class="container">
        <div class="jumbo-details">
          <p class="jumbo-main">Buy And Sell Your Car At Its Value</p>
          <p class="jumbo-second">Find the right price and dealer.</p>
          <p class="jumbo-second">Learn More -></p>
          <!--AGGIUNGERE ICONA FRECCIA -->
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;

.jumbo-details {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 0.8rem;
}
.jumbo {
  height: 100vh;
  background-image: url(../assets/img/slider-autocar-5.jpg);
  background-size: cover;
  color: $white-main;
  .jumbo-main {
    font-size: 3rem;
    font-weight: 800;
    max-width: 500px;
  }
  .jumbo-second {
    font-size: 1.3rem;
    font-weight: 600;
  }
}
</style>
