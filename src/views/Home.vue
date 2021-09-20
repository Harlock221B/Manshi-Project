<template>
  <div>
    <div class="home">
      <h1>Bem vindo ao <br> Roberto Manshi </h1>
    </div>
    <Cardinfo 
      text_title="Tratamento Especial!"
      text_content="Alguma coisa"
      back_color="black"
      text_color="white"
    />
  </div>
</template>

<script>
import Cardinfo from "../components/CardInfo.vue";

export default {
  name: "Home",
  components: {
    Cardinfo,
  },
};
</script>

<style scoped src="./Home.css">
</style>
