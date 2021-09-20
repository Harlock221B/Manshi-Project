<template>
  <div>
    <div class="home">
      <h1>
        Bem vindo ao <br />
        Roberto Manshi
      </h1>
    </div>
    <Cardinfo
      text_title="Tratamento Especial!"
      text_content="Alguma coisa"
      back_color="black"
      text_color="white"
      :imgs="my_imgs"
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
  data() {
    return {
      my_imgs: [] 
    }
  },

  methods: {
    async getImagesBackend() {
      const response = await fetch("http://localhost:3000/imgback");
      console.log(jsonData);
    }
  },

  mounted(){
    this.getImagesBackend();
  },
};
</script>

<style scoped src="./Home.css">
</style>
