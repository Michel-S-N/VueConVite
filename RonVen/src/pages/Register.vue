<template>
  <div>
    <div class="titulo-log">
      <button class="btn btn-outline-warning">Home</button>
    </div>
    <FormComp :titulo="'Registrarse'" :button="'Registrarse'" />
  </div>
</template>

<script>
import FormVue from "../components/Form.vue";

export default {
  components: {
    FormComp: FormVue,
  },
};
</script>

<style scoped>
.titulo-log {
  width: 100%;
  padding: 15px;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: row;
  gap: 5px;
}
</style>
