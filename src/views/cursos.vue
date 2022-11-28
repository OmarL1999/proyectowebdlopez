<template>
  <div>
    <v-row>
      <v-col>
        <h1 class="text-center">CURSO ONLINE</h1>
      </v-col>
    </v-row>
    <cursos />
  </div>
</template>

<script>
import cursos from "@/components/cursos.vue"
export default {
  components: {
    cursos
  }
}
</script>

<style>
</style>