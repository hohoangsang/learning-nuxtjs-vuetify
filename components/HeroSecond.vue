<template>
  <section id="hero-second">
    <v-row no-gutters>
      <v-img :src="require('~/assets/images/hero2.png')">
        <v-theme-provider dark>
          <v-container fill-height style="max-width: 850px">
            <v-row align="center" justify="center" class="white--text">
              <v-col tag="h2" class="text-center">Download the app now.</v-col>

              <v-col cols="12" class="text-center">
                <span>Available on your favorite store. Start your premium experience now</span>
              </v-col>

              <v-col cols="12" class="mx-auto" style="position: relative;">
                <div class="d-flex justify-center">
                  <v-btn class="mx-5" rounded style="background-color: #fa4a0c">
                    <span class="pa-4">Playstore</span>
                  </v-btn>

                  <v-btn class="mx-5" outlined rounded style="background-color: transparent">
                    <span class="pa-4">App store</span>
                  </v-btn>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-theme-provider>
      </v-img>
    </v-row>
  </section>
</template>

<script>
export default {
  name: 'HeroSecondComponent'
}
</script>

<style lang="scss" scoped></style>
