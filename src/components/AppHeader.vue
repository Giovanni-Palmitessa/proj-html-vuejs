<script>
import MenuList from "./MenuList.vue";

export default {
  data() {
    return {
      arrLiNavbar: [
        {
          number: 1,
          menuList: "Home",
        },
        {
          number: 2,
          menuList: "About Us",
        },
        {
          number: 3,
          menuList: "Vehicles",
        },
        {
          number: 4,
          menuList: "Dealers",
        },
        {
          number: 5,
          menuList: "Packages",
        },
        {
          number: 6,
          menuList: "Blog",
        },
        {
          number: 1,
          menuList: "Contact",
        },
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
    MenuList,
  },
};
</script>
<template>
  <header>
    <div class="container">
      <ul>
        <li>
          <a href="#"
            ><img src="../assets/img/logo-autocar11.png" alt="Logo Autocar"
          /></a>
        </li>
        <MenuList
          v-for="list in arrLiNavbar"
          :key="list.number"
          :menuList="list.menuList"
        />
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 70px;
}
</style>
