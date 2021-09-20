<template>
  <div class="app_div">
    <Navbar text_color="white" back_color="black" img_logo="/images/ramen.svg"/>
    <router-view />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
export default {
  name: "App",
  components: {
    Navbar,
  },
};
</script>

<style src="./App.css">
</style>
