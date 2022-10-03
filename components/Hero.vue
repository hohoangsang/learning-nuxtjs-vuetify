<template>
  <section id="hero" style="margin-bottom: 600px">
    <v-row no-gutters>
      <v-img :src="require('~/assets/images/hero.png')">
        <v-theme-provider dark>
          <v-container fill-height style="max-width: 950px">
            <v-row align="center" justify="center" class="white--text mx-auto">
              <v-col cols="12" tag="h1" class="text-center"> Bella Olonje </v-col>

              <v-col cols="12" class="text-center font-weight-black">
                <p style="font-size: 58px">Why stay hungry when you can order form Bella Onojie</p>
              </v-col>

              <v-col cols="12" class="text-center">
                <span>Download the bella onoje’s food app now on</span>
              </v-col>

              <v-col cols="12" class="mx-auto">
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

      <v-container>
        <div class="d-flex justify-center" style="max-width: 600px; position: relative; margin: 0 auto">
          <v-img
            :src="require('~/assets/images/iphone-left.png')"
            style="max-width: 500px; position: absolute; bottom: -500px; left: -30px; z-index: 1"
          ></v-img>
          <v-img
            :src="require('~/assets/images/iphone-right.png')"
            style="max-width: 285px; position: absolute; bottom: -450px; right: 50px"
          ></v-img>
        </div>
      </v-container>
    </v-row>
  </section>
</template>

<script>
export default {
  name: 'HeroComponent'
}
</script>
