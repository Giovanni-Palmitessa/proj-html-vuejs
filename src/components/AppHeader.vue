<script>
export default {
  data() {
    return {
      arrLiNavbar: [
        "Home",
        "About Us",
        "Vehicles",
        "Dealers",
        "Packages",
        "blog",
        "Contact",
      ],
      arrLiImgNavbar: [
        {
          img: "../assets/img/padlock.png",
          menuList: "My Account",
        },
        {
          img: "../assets/img/add.png",
          menuList: "Add Car",
        },
        {
          img: "../assets/img/headphones.png",
          menuList: "+1 (234) 567 89 10",
        },
      ],
    };
  },
};
</script>
<template>
  <header>
    <div class="container">
      <ul class="navbar">
        <li>
          <a href="#">
            <img src="../assets/img/logo-autocar11.png" alt="Logo Autocar" />
          </a>
        </li>
        <li>
          <a href="#">{{ navbarList }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 70px;
  img {
    width: 15%;
  }
}
</style>
