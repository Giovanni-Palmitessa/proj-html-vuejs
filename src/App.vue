<script>
import AppHeader from "./components/AppHeader.vue";

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
    AppHeader,
  },
};
</script>

<template>
  <AppHeader />
</template>

<style lang="scss">
@use "./assets/partials/general" as *;
</style>
