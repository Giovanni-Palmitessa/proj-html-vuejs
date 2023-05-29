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
img {
  width: 50%;
}
</style>
