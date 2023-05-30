<script>
export default {};
</script>
<template>
  <footer>
    <div class="container">
      <div class="footerContent">
        <div class="ftr-left">
          <img src="../assets/img/logo-footer-autocar11.png" alt="Autocar" />
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
  .footerContent {
    display: flex;
    gap: 3rem;
  }
}
</style>
