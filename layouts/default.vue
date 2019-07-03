<template>
    <v-app id="inspire">
        
        <!-- Nav -->
        <v-toolbar color="blue-grey" dark fixed app clipped-left>
            <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-title>Toolbar</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon large>
                <v-avatar size="32px" tile>
                    <img src="https://cdn.vuetifyjs.com/images/logos/logo.svg" alt="Vuetify">
                </v-avatar>
            </v-btn>
        </v-toolbar>
        <!-- fin del Nav -->
        
        <!-- Navbar -->
        <v-navigation-drawer v-model="drawer" fixed left clipped app>
            <v-list dense>
                <v-list-tile v-for="(item, i) in items" :key="i" :to="item.to" router exact>
                    <v-list-tile-action>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title v-text="item.title" />
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>
        <!-- Fin de Navbar -->

        <!-- contendo general de la aplicacion -->
        <v-content>
            <v-container>
                <nuxt />
            </v-container>
        </v-content>
        <!-- fin de contendor general  -->
        
        <!-- footer -->
        <v-footer color="blue-grey" class="white--text" app>
            <span>Glendy</span>
            <v-spacer></v-spacer>
            <span>&copy; 2019</span>
        </v-footer>
        <!-- fin del footer -->

    </v-app>
</template>

<script>
    import Logo from '~/components/Logo.vue'
    export default {
        data: () => ({
            drawer          : null,
            drawerRight     : null,
            right           : false,
            left            : false,
            items           : [
                {
                    icon    : 'apps',
                    title   : 'Welcome',
                    to      : '/'
                },
                {
                    icon    : 'bubble_chart',
                    title   : 'Inspire',
                    to      : '/inspire'
                },
                {
                    icon    : 'bubble_chart',
                    title   : 'Asistentes',
                    to      : '/asistentes'
                },
                {
                    icon    : 'bubble_chart',
                    title   : 'Ponentes',
                    to      : '/asistentes'
                }
            ]
        }),
        props: {
            source      : String
        }
    }
</script>