<template>
  <v-card class="my-6">
    <v-card-title class="yellow--text">
      Nome casa scommesse
    </v-card-title >
    <v-card-text>
      <v-row>
        <v-col md="6" lg="6" xs="6">
                <div>
        <h1>
          Bonus:
        </h1>
        <h2>
          Ciao
        </h2>
        <h2>
          Ciao
        </h2>
      </div>
        </v-col>
        <v-col md="6" lg="6" xs="6" class="pl-16" >
      <img height="100" src="../static/goldbetsport.png" class="justify-right"></img>
        </v-col>
      </v-row>

    </v-card-text>
    <v-card-actions>
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
