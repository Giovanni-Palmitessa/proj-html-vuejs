<script>
export default {
  props: {
    menuList: String,
  },
};
</script>
<template>
  <li>
    <a href="#">{{ menuList }}</a>
  </li>
</template>

<style lang="scss" scoped>
a {
  color: black;
  transition: all 0.5s ease-out;
  &:hover {
    color: darksalmon;
  }
}
</style>
