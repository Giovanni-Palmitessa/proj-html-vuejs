<script>
export default {
  props: {
    urlImg: String,
    menuListImg: String,
  },
};
</script>
<template>
  <li>
    <div class="black">
      <img :src="urlImg" :alt="menuListImg" />
      <a href="#">{{ menuListImg }}</a>
    </div>
  </li>
</template>

<style lang="scss" scoped>
li {
  .black {
    background-color: black;
    padding: 2rem;
    height: 50px;
    display: flex;
    align-items: center;
    gap: 10px;
    border-radius: 10px;
    img {
      width: 30px;
      filter: grayscale(1) invert(1);
    }
    a {
      color: white;
      font-weight: 600;
    }
  }
}
</style>
