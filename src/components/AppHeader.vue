<script>
export default {
  props: {
    urlImg: String,
    navbarList: String,
  },
};
</script>
<template>
  <header>
    <div class="container">
      <ul class="navbar">
        <li>
          <a href="#">
            <img src="../assets/img/logo-autocar11.png" alt="Logo Autocar" />
          </a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 70px;
}
</style>
