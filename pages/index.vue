<template>
    <v-layout column justify-center align-center>
        <v-flex xs12 sm8 md6>
            <div class="text-xs-center">
                <!-- <logo />
                <vuetify-logo /> -->
            </div>
            <v-card>
                <v-card-title class="headline">
                    Welcome to the Vuetify + Nuxt.js template
                </v-card-title>
                <v-card-text>
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Velit neque similique, impedit commodi placeat voluptatem nihil quas sed, dolorem assumenda ex tenetur, accusamus eius provident deserunt blanditiis consectetur est ipsum!
                </v-card-text>
                <v-card-actions>
                    <v-spacer />
                        <v-btn color="primary" flat nuxt to="/inspire">
                            Continue
                        </v-btn>
                        <v-btn color="primary" flat nuxt to="/asistentes">
                            Registro
                        </v-btn>
                </v-card-actions>
            </v-card>
        </v-flex>
    </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>
