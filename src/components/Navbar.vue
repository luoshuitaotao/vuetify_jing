<template>
    <nav>
        <v-toolbar flat app>
            <v-app-bar-nav-icon class="grey--text" @click="drawer=!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Todo</span>
                <span>Jing</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="lightgrey">
                <span>Sign out</span>
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer v-model="drawer" app class="primary">
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

