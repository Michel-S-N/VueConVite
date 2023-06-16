<template>
  <div class="bgHome">
    <div class="title">
      <button class="btn btn-outline-warning" @click="goTo('/registrarse')">
        Registrarse
      </button>
      <button class="btn btn-outline-warning" @click="goTo('/login')">
        Login
      </button>
      <button class="btn btn-outline-warning" @click="goTo('/car')">Car</button>
    </div>
    <CardComp :rons="Rons" />
  </div>
</template>

<script>
import Card from "../common/Card.vue";
import { Rons } from "../static/Rons";

export default {
  components: {
    CardComp: Card,
  },
  data() {
    return { Rons };
  },
  methods: {
    goTo(route) {
      this.$router.push(route);
    },
  },
};
</script>

<style scoped>
.bgHome {
  background: #000;
}
.title {
  width: 100%;
  padding: 15px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: row;
  gap: 5px;
}
</style>
