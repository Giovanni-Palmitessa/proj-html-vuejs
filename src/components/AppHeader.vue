<script>
import MenuList from "./MenuList.vue";
import MenuListImg from "./MenuListImg.vue";

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
          number: 7,
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
  methods: {
    getImagePath(img) {
      return new URL(img, import.meta.url).href;
    },
  },
  components: {
    MenuList,
    MenuListImg,
  },
};
</script>
<template>
  <header>
    <div class="container">
      <ul class="navbar">
        <li>
          <a href="#"
            ><img
              src="../assets/img/logo-autocar11.png"
              alt="Logo Autocar"
              class="logo"
          /></a>
        </li>
        <MenuList
          v-for="list in arrLiNavbar"
          :key="list.number"
          :menuList="list.menuList"
        />
        <MenuListImg
          v-for="listImg in arrLiImgNavbar"
          :key="listImg.menuList"
          :menuListImg="listImg.menuList"
          :urlImg="getImagePath(listImg.img)"
        />
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  .navbar {
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 0.5rem;
  }
  height: 70px;
  .logo {
    width: 40%;
  }
}
</style>
