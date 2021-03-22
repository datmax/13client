<template>
  <v-card class="my-6">
    <v-card-title class="yellow--text">
      Nome casa scommesse
    </v-card-title>
    <v-card-text>
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
    </v-card-text>
    <v-card-actions>
      <v-spacer />
      <a :href="link" e>
        <v-btn color="yellow" class="black--text">
          Entra
          <v-icon
            color="black "
          >
            mdi-message-text
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
    }

  }
}
</script>
