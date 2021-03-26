<template>

    <v-form>
        <v-row justify="space-between">
          <v-col >
            <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="asdfasdf"
                required
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"

            ></v-text-field>
            <v-select
                v-model="tipoDocu"
                :items="tipoDocumento"
                :error-messages="selectErrors"
                label="Item"
                required


            ></v-select>
          </v-col>
          <v-col>
            <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="E-mail"
                required
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"

            ></v-text-field>
            <v-select
                v-model="prod"
                :items="producto"
                :error-messages="selectErrors"
                label="Item"
                required
                @change="$v.select.$touch()"
                @blur="$v.select.$touch()"

            ></v-select>
          </v-col>





        <v-btn block append>HOLA</v-btn>
      </v-row>
    </v-form>

</template>

<script lang="js">

export default {

  name: "FormFiltro",


}
</script>


<style scoped>

</style>