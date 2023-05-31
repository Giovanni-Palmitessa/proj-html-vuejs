<script>
import FooterLinksAccount from "./FooterLinksAccount.vue";
import FooterLinksQuick from "./FooterLinksQuick.vue";

export default {
  data() {
    return {
      arrMyAccount: [
        {
          liFtr: "My account",
        },
        {
          liFtr: "Checkout",
        },
        {
          liFtr: "Cart",
        },
        {
          liFtr: "Packages",
        },
        {
          liFtr: "Add Car",
        },
      ],
      arrQuickLinks: [
        {
          liFtr: "Home",
        },
        {
          liFtr: "About Us",
        },
        {
          liFtr: "Blog",
        },
        {
          liFtr: "Contact",
        },
        {
          liFtr: "Refund & Returns",
        },
      ],
    };
  },
  components: {
    FooterLinksAccount,
    FooterLinksQuick,
  },
};
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
        <div class="ftr-center">
          <h2>Join Our Newsletter</h2>
          <p>Subscribe to be informed about our services and products.</p>
          <input type="email" placeholder="Your Email Adress" />
          <div class="white-btn">Subscribe</div>
        </div>
        <div class="ftr-right">
          <div class="myAccount">
            <h2>My Account</h2>
            <ul class="list">
              <FooterLinksAccount
                v-for="links in arrMyAccount"
                :key="links.liFtr"
                :links="links.liFtr"
              />
            </ul>
          </div>

          <div class="quickLinks">
            <h2>Quick Links</h2>
            <ul class="list">
              <FooterLinksQuick
                v-for="links in arrQuickLinks"
                :key="links.liFtr"
                :links="links.liFtr"
              />
            </ul>
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
      flex-basis: 30%;
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
    .ftr-center {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      flex-basis: 40%;
      p {
        font-size: 0.8rem;
      }
      input {
        padding: 1.3rem;
        border-radius: 5px;
      }
      .white-btn {
        background-color: $white-main;
        text-align: center;
        color: $gray-main;
        padding: 1.3rem;
        &:hover {
          cursor: pointer;
        }
      }
    }
    .ftr-right {
      display: flex;
      gap: 3rem;
      flex-basis: 30%;
      h2 {
        margin-bottom: 1rem;
      }
      .list {
        list-style: square;
        list-style-position: inside;
      }
    }
  }
}
</style>
