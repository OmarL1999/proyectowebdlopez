<template>
  <div>
    <v-row>
      <v-card name="n1" class="mx-auto" max-width="344">
        <v-img
          src="https://prod-discovery.edx-cdn.org/media/course/image/bcf6db1c-0a69-42d1-b830-425d81863eb6-82347756370a.small.png"
          height="200px"></v-img>
        <v-card-title>
          Programación para todos
        </v-card-title>
        <v-card-subtitle>
          (empezando con Python)
        </v-card-subtitle>
        <v-card-actions>
          <v-btn color="orange lighten-2" text>
            Ver Mas
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn icon @click="show = !show">
            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>
        <v-expand-transition>
          <div v-show="show">
            <v-divider></v-divider>
            <v-card-text>
              Este curso en línea es una introducción "sin prerrequisitos" a la programación en Python. Aprenderás sobre
              las variables, la ejecución condicional, la ejecución repetida y cómo usamos las funciones.
            </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
      <v-card name="n2" class="mx-auto" max-width="344">
        <v-img
          src="https://prod-discovery.edx-cdn.org/media/course/image/fa82aec4-f617-4efc-b64e-2855f1567df4-3c78499bb9f8.small.png"
          height="200px"></v-img>
        <v-card-title>
          Machine Learning
        </v-card-title>
        <v-card-subtitle>
          (aprendizaje automático) con Python: una introducción práctica
        </v-card-subtitle>
        <v-card-actions>
          <v-btn value="c" color="orange lighten-2" text>
            Ver Mas
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn icon @click="show1 = !show1">
            <v-icon>{{ show1 ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>
        <v-expand-transition>
          <div v-show="show1">
            <v-divider></v-divider>
            <v-card-text>
              El Machine Learning puede ser una herramienta increíblemente beneficiosa para descubrir información y
              predecir tendencias futuras. Este curso de aprendizaje automático con Python te brindará todas las
              herramientas que necesitas para comenzar con el aprendizaje supervisado y autónomo. </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
      <v-card name="n3" class="mx-auto" max-width="344">
        <v-img
          src="https://prod-discovery.edx-cdn.org/media/course/image/019dd154-cb89-4a24-aed5-f0b8db33d705-84fd16f1a8ca.small.jpg"
          height="200px"></v-img>
        <v-card-title>
          Android
        </v-card-title>
        <v-card-subtitle>
          Introducción a la Programación
        </v-card-subtitle>
        <v-card-actions>
          <v-btn value="c" color="orange lighten-2" text>
            Ver Mas
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn icon @click="show3 = !show3">
            <v-icon>{{ show3 ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>
        <v-expand-transition>
          <div v-show="show3">
            <v-divider></v-divider>
            <v-card-text>
              Desarrollaremos una aplicación de ejemplo, "Mis Lugares Favoritos," para conocer el entorno de desarrollo
              de Android y sus elementos.. </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    show: false,
    show1: false,
    show3: false,
  }),
}
</script>