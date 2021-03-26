<template>
  <v-app>
    <!--NAVBAR-->
    <v-app-bar app color="primary" dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" ></v-app-bar-nav-icon>
      <v-app-bar-title>
        HOLA
      </v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn class="error">Salir</v-btn>
    </v-app-bar>
    <!--MENU LATERAL-->
    <v-navigation-drawer app temporary dark v-model="drawer">
      <v-layout mt-4 column align-center>
        <v-flex>
          <v-avatar>
            <img   src="https://cdn.vuetifyjs.com/images/john.jpg">
          </v-avatar>
        </v-flex>
        <v-flex>
          <p class="white--text">Esteban Foffano</p>
        </v-flex>
      </v-layout>
      <v-layout column  >
        <v-flex mx3>
          <v-btn  color="primary" block :to="{name: 'home'}" >Home</v-btn><br>
          <v-btn  color="primary" block :to="{name: 'grid'}">Tabla con filtro</v-btn>
        </v-flex>
      </v-layout>
    </v-navigation-drawer>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    drawer: true,
  }),
};
</script>
