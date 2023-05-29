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

<style lang="scss" scoped></style>
