<template>
    <nav>
        <v-toolbar app dark>
            <v-toolbar-side-icon @click="sidemenu = !sidemenu"></v-toolbar-side-icon>
            <v-toolbar-title class="headline text-uppercase">
                <span>Louisoix </span>
                <span class="font-weight-light">| An FFXIV Tool</span>
            </v-toolbar-title>

            <v-spacer></v-spacer>

            <v-btn flat href="https://github.com/CannoliSquid/louisoix-electron" target="_blank">
                <span class="mr-2">GitHub</span>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer app v-model="sidemenu" class="grey darken-3">
            <v-list>
                <v-list-tile v-for="link in links" :key="link.text">
                    <v-list-tile-action>
                        <v-icon class="white--text">{{ link.icon }}</v-icon>
                    </v-list-tile-action>
                    <v-list-title-content>
                        <v-list-tile-title class="white--text">
                            {{ link.text }}
                        </v-list-tile-title>
                    </v-list-title-content>
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            sidemenu: false,
            links: [
                {icon: 'home', text: 'Home', route:'/'},
                {icon: 'search', text: 'Search', route:'/search'},
                {icon: 'info', text: 'About', route:'/about'},
            ]
        }
    }
}
</script>
