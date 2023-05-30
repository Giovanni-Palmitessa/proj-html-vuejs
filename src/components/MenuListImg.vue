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
    <img :src="urlImg" :alt="menuListImg" />
    <a href="#">{{ menuListImg }}</a>
  </li>
</template>

<style lang="scss" scoped>
li {
  background-color: black;
  padding: 2rem;
}
a {
  color: white;
}
img {
  width: 30px;
}
</style>
