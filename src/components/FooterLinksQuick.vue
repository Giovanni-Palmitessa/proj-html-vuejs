<script>
export default {
  props: {
    links: String,
  },
};
</script>
<template>
  <li>
    <a href="#">{{ links }}</a>
  </li>
</template>

<style lang="scss" scoped>
a {
  color: white;
}
li {
  line-height: 30px;
}
</style>
