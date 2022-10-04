<template>
  <div>
    <HeroFirst />

    <v-container style="max-width: 885px">
      <v-divider />
    </v-container>

    <h3
      class="text-h3 text-center font-weight-medium"
      style="margin-top: 72px; margin-bottom: 59px"
    >
      How the app works
    </h3>

    <!-- main content -->
    <v-container>
      <v-row
        justify="space-around"
        align="center"
        no-gutters
        v-for="(content, i) in mainContent"
        :key="i"
        :class="[content.isReverse ? 'flex-row-reverse' : null]"
        style="margin-bottom: 200px"
      >
        <v-img
          style="
            width: 100%;
            max-width: 300px;
            filter: drop-shadow(50px 30px 150px rgba(46, 4, 4, 0.15));
          "
          :src="require('~/assets/images/main-pic2.png')"
          :alt="content.title"
        />
        <div style="max-width: 560px">
          <h5 class="text-h6 my-4" style="color: #fa4a0c; line-height: calc(36 / 24)">
            {{ content.title }}
          </h5>
          <p class="font-weight-bold" style="line-height: calc(57 / 40); font-size: 40px">
            {{ content.description }}
          </p>
          <span
            class="font-weight-light"
            style="display: block; max-width: 467px; font-size: 24px"
            >{{ content.span }}</span
          >
        </div>
      </v-row>
    </v-container>

    <HeroSecond />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  data () {
    return {
      mainContent: [
        {
          title: 'Create an account',
          description: 'Create/login to an existing account to get started',
          span: 'An account is created with your email and a desired password',
          imageLink: '~/assets/images/main-pic1.png',
          isReverse: false
        },
        {
          title: 'Explore varieties',
          description: 'Shop for your favorites meal as e dey hot.',
          span: 'Shop for your favorite meals or drinks and enjoy while doing it.',
          imageLink: '~/assets/images/main-pic2.png',
          isReverse: true
        },
        {
          title: 'Checkout',
          description: 'When you done check out and get it delivered.',
          span: 'When you done check out and get it delivered with ease.',
          imageLink: '~/assets/images/main-pic3.png',
          isReverse: false
        }
      ]
    }
  }
}
</script>
