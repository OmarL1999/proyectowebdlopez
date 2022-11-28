<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-spacer></v-spacer>
      <v-btn v-for="(item, index) in rutas" :key="index" text @click="insertarRuta(item.ruta)">
        <span class="mr-2">{{ item.nombre }}</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    rutas: [
      { nombre: 'Home', ruta: '/' },
      { nombre: 'About', ruta: '/about' },

      //{nombre:'Cursos Online', ruta:'/imagenes'},
      { nombre: 'Registrar', ruta: '/registro' },
      { nombre: 'Login', ruta: '/login' }

    ]
  }),

  methods: {
    insertarRuta(ruta) {
      this.$router.push(ruta);

    }
  }

};
</script>
