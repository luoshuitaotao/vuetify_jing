<template>
    <nav>
        <v-toolbar flat app>
            <v-app-bar-nav-icon class="grey--text" @click="drawer=!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Todo</span>
                <span>Jing</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-menu offset-y>
                <template v-slot:activator="{ on, attrs }">
                    <v-btn flat color="grey" dark v-bind="attrs" v-on="on">
                    <span>MENU</span>
                    </v-btn>
                </template>
                <v-list>
                    <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                        <v-list-item-title>{{ link.text }}</v-list-item-title>
                    </v-list-item>
                </v-list>
            </v-menu>

            <v-btn flat color="grey">
                <span>Sign out</span>
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer v-model="drawer" app class="primary">
            <v-layout column align-center>
                <v-flex class= "mt-5">
                    <v-avatar size= "100">
                        <img src="/avatar-1.png">
                    </v-avatar>
                    <p class="white--text subheading mt-1">
                        The Net Ninga
                    </p>
                </v-flex>
            </v-layout>
            <v-list dark>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-tile-action>
                        <v-icon>{{ link.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-item-title>{{ link.text }}</v-list-item-title>
                    </v-list-tile-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>
<script>
export default {
    data(){
        return{
            drawer:false,
            links:[
              { icon: 'mdi-view-dashboard', text: 'Dashboard', route: '/' },
              { icon: 'mdi-folder', text: 'My Projects', route: '/projects' },
              { icon: 'mdi-account', text: 'Team', route: '/team' },
            ]
        }
    }
    
}
</script>

