<template>
  <v-footer>
    <v-container>
      <v-row justify="space-between" align="cener">
        <img
          srcset="@/assets/images/bella-olonje.png 2x"
          alt="Bella olonje"
          contain
          class="ma-5"
          style="width: 100%; max-width: 246px"
        />

        <div class="d-flex justify-center align-center">
          <img srcset="~/assets/images/twitter.png 2x" />
          <img srcset="~/assets/images/facebook.png 2x" />
          <img srcset="~/assets/images/instagram.png 2x" />
        </div>

        <p class="font-weight-bold ma-auto" style="font-size: 12px; line-height: calc(18 / 12)">
          Copywright 2020 Bella Onojie.com
        </p>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: 'FooterComponent',
  data () {
    return {
      socialList: [
        { name: 'twitter', src: '~/assets/images/twitter.png' },
        { name: 'facebook', src: '~/assets/images/facebook.png' },
        { name: 'instagram', src: '~/assets/images/instagram.png' }
      ]
    }
  }
}
</script>
