<template>

    <v-jumbotron>
        <v-img
            src="https://png.pngtree.com/thumb_back/fw800/back_our/20190620/ourmid/pngtree-electronic-technology-website-texture-background-banner-image_156039.jpg"
            class="my-3" contain height="450" />

        <v-container fill-height>
            <v-layout align-center>
                <v-flex>

                    <h3 class="display-3">CURSOS EN LINEA GRATUITOS</h3>

                    <span class="subheading">Todas las personas tienen el potencial de generar cambios, ya sea en su
                        vida, su comunidad o el mundo. Y es el poder transformador de la educación lo que revela ese
                        potencial. Sin embargo, únicamente los miembros de grupos privilegiados han tenido acceso a una
                        educación de alta calidad. En 2012, nos dimos cuenta de que era el momento de hacer un cambio
                        radical en el aprendizaje. De lo ya probado a lo novedoso. De un acceso "limitado" a un acceso
                        "ilimitado". Al abrir el aula a través del aprendizaje en línea, edX permite que millones de
                        estudiantes liberen su potencial y se conviertan en agentes de cambio.</span>

                    <v-divider class="my-3"></v-divider>

                    <div class="title mb-3">Revisa todos nuestros Cursos!</div>

                    <v-btn class="mx-0" color="primary" large @click="insertarRuta('login')">
                        Ver mas
                    </v-btn>
                </v-flex>
            </v-layout>
        </v-container>
    </v-jumbotron>

</template>

<script>
export default {
    data: () => ({
        gradient: 'to top right, rgba(63,81,181, .7), rgba(25,32,72, .7)'
    }),

    methods: {
        insertarRuta(ruta) {
            this.$router.push(ruta);

        }
    }


}

</script>


<style>

</style>