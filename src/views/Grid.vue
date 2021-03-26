<template>
  <v-container grid-list-md>
    <FormFiltro></FormFiltro>

    <Tabla></Tabla>
  </v-container>
</template>
<script>
import Tabla from "@/components/Tabla";
import FormFiltro from "@/components/FormFiltro";
export default {
  components: {FormFiltro, Tabla}
}
</script>