<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6 ">
      <div class="text-center">
        <h1 class="border">
          Link utili
        </h1>
      </div>
      <div class="text-left">
        <h1 class="yellow--text">
          Bonus:
        </h1>
        <bonus-card title="ciao" link="https://www.google.com" description="ciao" total-bonus="500" />
        <bonus-card title="ciao" link="https://www.google.com" description="ciao" total-bonus="500" />
        <h1 class="yellow--text">
          Canali telegram:
        </h1>

        <telegram-card title="ciao" link="https://www.google.com" description="ciao" total-bonus="500" />
      </div>
    </v-col>
  </v-row>
</template>

<script>
import BonusCard from '../components/BonusCard.vue'
import TelegramCard from '../components/TelegramCard.vue'
export default {
  components: {
    BonusCard,
    TelegramCard
  },
  head () {
    return {
      title: '13Tipster'
    }
  }
}
</script>
<style>
h2, h1{
  margin-bottom: 2px;
}
</style>
