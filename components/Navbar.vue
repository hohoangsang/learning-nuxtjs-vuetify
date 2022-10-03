<template>
  <v-app-bar app fixed height="120" flat hide-on-scroll dense class="bgNav">
    <img srcset="@/assets/images/bella-olonje.png 2x" alt="Bella olonje" contain class="ma-5" />

    <v-spacer />

    <v-hover v-for="link in linkList" :key="link.href" v-slot="{ hover }" class="ma-4">
      <v-btn
        nuxt
        :to="link.href"
        tile
        plain
        :style="hover && 'border-bottom: 2px solid red; color: red'"
        exact-active-class="red--text active-link"
      >
        {{ link.text }}
      </v-btn>
    </v-hover>

    <v-spacer />

    <v-switch
      v-model="$vuetify.theme.dark"
      class="mx-4"
      inset
      persistent-hint
      hide-details
      label="Dark mode"
    />

    <v-hover v-slot="{ hover }" class="ma-4">
      <v-btn tile plain :style="hover && 'color: red'">
        <span>Login</span>
        <v-icon right> mdi-login </v-icon>
      </v-btn>
    </v-hover>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavbarComponent',

  data () {
    return {
      linkList: [
        { text: 'Home', href: '/' },
        { text: 'About', href: '/about' },
        { text: 'Contact', href: '/contact' },
        { text: 'News', href: '/news' }
      ]
    }
  },

  mounted () {
    const url = new URL(window.location)

    console.log(url)
  }
}
</script>

<style scoped>
    .active-link {
        border-bottom: 2px solid red;
    }
</style>
