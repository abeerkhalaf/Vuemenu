<template>
    <nav>
       <v-toolbar flat app>
          <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
<v-toolbar-title class="text-uppercase grey--text">
    <span class="font-weight-light">China</span>
    <span>Doto</span>
</v-toolbar-title>
           <v-spacer></v-spacer>
           <v-btn flat color="grey lighten-4">
               <span>Sign out</span>
               <v-icon right>exit_to_app</v-icon>
           </v-btn>
       </v-toolbar>

        <v-navigation-drawer app v-model="drawer"  absolute temporary class="primary">
            <v-list-item  v-for="link in links" :key="link.text" router :to="link.route">
               <v-list-tile-action>
                    <v-icon class="white--text">{{link.icon}}</v-icon>
                </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title class="white--text">{{link.text}}</v-list-tile-title>
                    </v-list-tile-content>
            </v-list-item>
        </v-navigation-drawer>
    </nav>
</template>

<script>
    export default {
        data() {
            return {
                drawer:false,
                links: [
                    {icon: 'dashboard', text: 'Dashboard', route: '/'},
                    {icon: 'folder', text: 'My Projects', route: '/projects'},
                    {icon: 'person', text: 'Team', route: '/team'},
                ]
            }
        }

    }
</script>