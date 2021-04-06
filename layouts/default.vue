<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      temporary
      app
    >
      <v-list>
        <v-list-item>
          <img lazy-src="~/assets/logo.webp" src="~/assets/logo.webp" class="w200 mb-2" >
        </v-list-item>
        <v-divider />
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon color="yellow">
              {{ item.icon }}
            </v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar app dense>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <v-img lazy-src="/logo.webp" src="/logo.webp" max-width="500" class="mb-2 mx-auto" />

        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      app
      absolute
    >
      Il gioco è vietato ai minori e può causare dipendenza patologica - <a href="https://www.adm.gov.it/portale/monopoli/giochi/probabilita-vincita"> probabilità di vincita</a>

      <v-spacer />
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: true,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-account',
          title: 'Chi siamo',
          to: '/about'
        },
        {
          icon: 'mdi-check-decagram',
          title: 'Affiliazioni',
          to: '/affiliazioni'
        }
      ],
      miniVariant: true
    }
  }
}
</script>
<style>
.border{
  border-bottom: 1px solid yellow;
}
#app {

font-family: acumin-pro, sans-serif;

font-weight: 700;

font-style: italic;

}

.w200{
  max-width: 200px;
}
</style>
