<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      fixed
      app
    >
      <v-list>
        <v-list-item @click="()=> miniVariant = !miniVariant">
          <v-list-item-action>
            <v-icon color="yellow">
              mdi-menu
            </v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Menu</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
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

    <v-main>
      <v-container>
        <div class="img mx-auto">
          <v-img lazy-src="/logo.png" src="/logo.png" max-width="200" />
        </div>

        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
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
      drawer: true,
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
</style>
