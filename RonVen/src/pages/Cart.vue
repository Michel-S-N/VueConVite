<template>
  <div class="log">
    <div class="titulo-log">
      <button class="btn btn-outline-warning">Home</button>
      >
    </div>
    <FormComp :titulo="'Carrito'" :button="'Ingresar'" />
  </div>
</template>

<script>
import Form from "../components/Form.vue";

export default {
  components: {
    FormComp: Form,
  },
};
</script>
