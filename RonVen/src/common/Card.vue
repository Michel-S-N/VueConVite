<script>
export default {
  props: {
    rons: {
      type: Array,
      required: true,
    },
  },
};
</script>

<template>
  <div v-for="ron in rons" :key="ron.id" class="container">
    <img :src="ron.img" :alt="ron.titulo" class="containerImg" />

    <div class="containerCard">
      <h1 class="fontCardTituloPrincipal">Ron</h1>
      <h1 class="fontCardTitulo">{{ ron.titulo }}</h1>

      <div class="marginText">
        <span class="fontCardSubTitulo"> {{ ron.descripcion }}</span>
        <button class="fontCardPrecio marginText buttonStyle">
          Add to cart - ${{ ron.valor }}
        </button>
      </div>
    </div>
  </div>
</template>

<style>
.container {
  border: 1px solid black;
  display: flex;
  background-color: rgb(235, 215, 206);

  flex-direction: row;
  flex-wrap: wrap;
  width: 100%;
  height: 100vh;
}
.containerImg {
  width: 50%;
  height: 100%;
}
.containerCard {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  margin-left: 4%;
  margin-right: 4%;
  width: 40%;
  background-color: rgb(235, 215, 206);
}
.marginText {
  margin-top: 13%;
}
.buttonStyle {
  cursor: pointer;
  width: 100%;
  border-radius: 20px;
  background-color: #853d01;
}
@media (min-width: 320px) and (max-width: 850px) {
  .container {
    flex-wrap: wrap;
    height: auto;
  }
  .containerImg {
    width: 100%;

    height: auto;
  }
  .containerCard {
    width: 100%;
    margin-left: 0;
    margin-right: 0;
  }
  .marginText {
    margin-top: 3%;
  }
}
</style>
