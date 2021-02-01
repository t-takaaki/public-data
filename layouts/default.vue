<template>
  <div id="app">
    <v-app id="inspire">
      <v-app id="inspire">
        <v-navigation-drawer
          v-model="drawer"
          app
        >
          <v-list>
            <v-list-item nuxt to="/">
              <v-list-item-action>
                <v-icon>mdi-home</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Home
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-list-item nuxt to="/japan">
              <v-list-item-action>
                <v-icon>mdi-earth</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>
                  Japan
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-navigation-drawer>
    
        <v-app-bar
          app
        >
          <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          <v-toolbar-title>Public Data / Global Gender Gap Report</v-toolbar-title>
        </v-app-bar>
    
        <v-main>
          <v-container
            class="fill-height"
            fluid
          >
            <v-row
              align="center"
              justify="center"
            >
              <v-col class="text-center">
                <Nuxt />
              </v-col>
            </v-row>
          </v-container>
        </v-main>
        <v-footer
          app
        >
          <span>&copy; {{ new Date().getFullYear() }}</span>
        </v-footer>
      </v-app>
    </v-app>
  </div>
</template>

<script>
export default {
  loading: true,
  data() {
    return {
      drawer: null,
    }
  },
}
</script>
