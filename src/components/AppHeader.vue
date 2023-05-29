<script>
import HeaderNavbar from "./HeaderNavbar.vue";

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
  components: {
    HeaderNavbar,
  },
};
</script>
<template>
  <header>
    <div class="container">
      <HeaderNavbar />
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 70px;
}
</style>
