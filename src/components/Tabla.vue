<template>
  <v-data-table
      :headers="headers"
      :items="usuarios"
      :items-per-page="10"
      :search="search"
      item-key="id">

    <template v-slot:[`item.actions`]="{ item }">
      <v-icon
          small
          @click="deleteItem(item)"
      >
        mdi-delete
      </v-icon>
    </template>
  </v-data-table>
</template>

<script>
export default {
  data: () => ({

    usuarios: [
      {

        id: "f1",
        nombre: "nombre1.pdf",
        fecha: "2021-03-10"
      },
      {

        id: "f2",
        nombre: "nombre2.pdf",
        fecha: "2021-03-10"
      },
      {

        id: "f3",
        nombre: "nombre3.pdf",
        fecha: "2021-03-10"
      },
    ],
    headers :[
      {
        text: 'Id',
        align: 'start',
        sortable: true,
        value: 'id'
      },
      {
        text: 'Nombre de formulario',
        align: 'start',
        sortable: true,
        value: 'nombre'
      },
      {
        text: 'Fecha de subida',
        align: 'start',
        sortable: true,
        value: 'fecha'
      },
      {
        text: 'Actions',
        value: 'actions',
        sortable: false
      }
    ]


})

}
</script>

<style scoped>

</style>