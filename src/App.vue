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
