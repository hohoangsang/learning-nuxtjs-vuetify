<template>
  <v-app-bar app fixed height="100" flat hide-on-scroll dense class="bgNav">
    <img srcset="@/assets/images/bella-olonje.png 2x" alt="Bella olonje" contain />

    <v-spacer />

    <div>
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </div>

    <v-spacer />

    <v-hover :v-slot="{ hover }">
      <v-btn plain :class="['hover ? red--text : null']">
        <span>Login</span>
        <v-icon right>mdi-login</v-icon>
      </v-btn>
    </v-hover>

    <v-switch
      v-model="$vuetify.theme.dark"
      class="mx-4"
      inset
      persistent-hint
      hide-details
      label="Dark mode"
    />
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavbarComponent'
}
</script>
