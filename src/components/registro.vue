<template>
    <div mb-5>
        <v-form ref="form" v-model="valid" lazy-validation>
            <v-card class="mx-auto" max-width="600" color="#0002">
                <v-card-text>
                    <center>
                        <h1>Registro</h1>
                    </center>
                    <v-text-field v-model="name" :counter="10" :rules="nameRules" label="Nombres" required></v-text-field>
                    <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
                    <v-text-field v-model="password" :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
            :rules="[rules.required, rules.min]" :type="show1 ? 'text' : 'password'" name="input-10-1"
            label="Contraseña" hint="At least 8 characters" counter @click:append="show1 = !show1"></v-text-field>
                    <v-select v-model="select" :items="items" :rules="[v => !!v || 'Item is required']" label="Seleccione"
                        required></v-select>
                    <v-checkbox v-model="checkbox" :rules="[v => !!v || 'You must agree to continue!']"
                        label="Do you agree?" required></v-checkbox>
                    <v-btn  :disabled="!valid" color="success" class="mr-4" @click="validate('login')"  >
                        Validate
                    </v-btn>
                    <v-btn color="error" class="mr-4" @click="reset">
                        Reset Form
                    </v-btn>
                </v-card-text>
            </v-card>
        </v-form>
    </div>
</template>

<script>
export default {
    data: () => ({
        valid: true,
        name: '',
        nameRules: [
            v => !!v || 'Name is required',
            v => (v && v.length <= 55) || 'Name must be less than 10 characters',
        ],
        email: '',
        emailRules: [
            v => !!v || 'E-mail is required',
            v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
        ],
        show1: false,
    password: '',
    rules: {
      required: value => !!value || 'Required.',
      min: v => v.length >= 8 || 'Min 8 characters',
      emailMatch: () => (`The email and password you entered don't match`),
    },
        select: null,
        items: [
            'Estudiante',
            'Docente',
        ],
        checkbox: false,
    }),
    methods: {
        validate(ruta) {
            this.$refs.form.validate()
            this.$router.push(ruta)
        },
        reset() {
            this.$refs.form.reset()
        },
        
    
    },
}
</script>