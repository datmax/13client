<template>
  <v-card outlined elevation="4" color="blue-grey darken-4" class="my-6">
    <v-card-title class="yellow--text name">
      <h1>
        {{ name }}
      </h1>
      <v-spacer />
      Fino a €{{ totalBonus }}
    </v-card-title>
    <v-card-text>
      <v-row>
        <v-col md="6" lg="6" xs="6">
          <div>
            <h2 class="white--text pb-5">
              {{ title }}
            </h2>
            <h3>
              {{ description }}
            </h3>
          </div>
        </v-col>
        <v-col md="6" lg="6" xs="6" class="pl-16">
          <v-img max-height="300" :lazy-src="'/low' + image" :src="'/' + image" justify="center" />
        </v-col>
      </v-row>
    </v-card-text>
    <v-card-actions>
      <a href="https://www.casino-sicuro.it/advs/?ql=1546&fromdom=tipster-13th.tipsterspace" class="pl-1"><p>SI APPLICANO T&C</p></a>
      <v-spacer />
      <a :href="link" e>
        <v-btn color="yellow" class="black--text">
          Ottieni bonus
          <v-icon
            color="black "
          >
            mdi-arrow-right-thick
          </v-icon>
        </v-btn>
      </a>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    link: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    totalBonus: {
      type: String,
      required: true
    }
  }

}
</script>
