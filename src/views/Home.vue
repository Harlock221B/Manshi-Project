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
      text_content="Sint officia eiusmod aliquip mollit duis adipisicing. Exercitation id proident labore adipisicing voluptate eu sint culpa id nulla enim reprehenderit anim id. Anim eu commodo ullamco qui id laborum dolor deserunt exercitation. Do commodo occaecat eiusmod cupidatat ea voluptate quis cillum irure veniam exercitation."
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
      my_imgs: [],
    }
  },

  methods: {
    async getImagesBackend() {
      const response = await fetch("http://localhost:3000/imgback");
      const jsonData = await response.json();
      console.log(jsonData);

      for(let i=0; i<jsonData.length; i++){
        console.log(jsonData[i].img);
        this.my_imgs.push(jsonData[i].img);
      }
      console.log(this.my_imgs);
    }
  },

  mounted(){
    this.getImagesBackend();
  },
};
</script>

<style scoped src="./Home.css">
</style>
