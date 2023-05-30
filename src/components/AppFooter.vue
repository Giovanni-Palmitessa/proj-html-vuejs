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
            <font-awesome-icon icon="fa-solid fa-location-dot" class="icon" />
            <p>New Jersey,USA</p>
          </div>

          <div class="contact">
            <font-awesome-icon icon="fa-solid fa-phone-volume" class="icon" />
            <p>+1 (234) 567 89 10</p>
          </div>

          <div class="contact">
            <font-awesome-icon icon="fa-solid fa-envelope" class="icon" />
            <p>example@example.com</p>
          </div>

          <div class="socials">
            <a href="#"
              ><font-awesome-icon icon="fa-brands fa-facebook" class="icon"
            /></a>
            <a href="#"
              ><font-awesome-icon
                icon="fa-brands fa-square-instagram"
                class="icon"
            /></a>
            <a href="#"
              ><font-awesome-icon
                icon="fa-brands fa-square-twitter"
                class="icon"
            /></a>
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
      img {
        width: 40%;
        margin-bottom: 1rem;
      }
      .contact {
        display: flex;
        gap: 10px;
        margin-bottom: 1rem;
        .icon {
          font-size: 1.5rem;
        }
      }
      .socials {
        display: flex;
        gap: 15px;
        font-size: 1.5rem;
        a {
          color: $white-main;
        }
      }
    }
  }
}
</style>
