<template>
  <v-container>
    <v-row class="text-center">
      <v-carousel height="200" hide-delimiters>
        <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src"></v-carousel-item>
      </v-carousel>
      <v-col cols="12">
        <v-img :src="require('../assets/LOGO-ULEAM-VERTICAL.png')" class="my-3" contain height="300" />
      </v-col>
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Bienvenido a la mejor plataforma de Cursos Online
        </h1>
        <p class="subheading font-weight-regular">
          Esta es una plataforma desarrollada por la Uleam,
          <br>Para mas informacion
          <a href="https://www.uleam.edu.ec" target="_blank">Click Aqui</a>
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      items: [
        {
          src: 'https://prod-discovery.edx-cdn.org/media/course/image/bcf6db1c-0a69-42d1-b830-425d81863eb6-82347756370a.small.png',

        },
        {
          src: 'https://prod-discovery.edx-cdn.org/media/course/image/fa82aec4-f617-4efc-b64e-2855f1567df4-3c78499bb9f8.small.png',
        },
        {
          src: 'https://prod-discovery.edx-cdn.org/media/course/image/019dd154-cb89-4a24-aed5-f0b8db33d705-84fd16f1a8ca.small.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
    }
  },
}
</script>




