<template>
    <v-footer dark padless>
        <v-card flat tile class="indigo lighten-1 white--text text-center">
            <v-card-text>
                <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
                    <v-icon size="20px">
                        {{ icon }}
                    </v-icon>
                </v-btn>
            </v-card-text>
            <v-card-text class="white--text pt-1">
   _______________________________________________________________________________________________________________________________________________________________________________________________________
            </v-card-text>
            <v-divider></v-divider>
            <v-card-text class="white--text">
                {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
            </v-card-text>
        </v-card>
    </v-footer>
</template>

<script>
export default {

}
</script>

<style>

</style>