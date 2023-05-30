<script>
export default {};
</script>
<template>
  <footer>
    <div class="container">
      <div class="footerContent">
        <div class="ftr-left">
          <img src="../assets/img/logo-footer-autocar11.png" alt="Autocar" />
          <div class="contact">
            <font-awesome-icon icon="fa-solid fa-location-dot" />
            <p>New Jersey,USA</p>
          </div>
          <div class="contact">
            <font-awesome-icon icon="fa-solid fa-phone-volume" />
            <p>+1 (234) 567 89 10</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../assets/partials/variables" as *;

footer {
  background-color: $black-main;
  padding: 2rem;
  color: white;
  .footerContent {
    display: flex;
    gap: 3rem;
    .ftr-left {
      display: flex;
      flex-direction: column;
      .contact {
        display: flex;
        gap: 10px;
        margin-bottom: 1rem;
      }
    }
  }
}
</style>
