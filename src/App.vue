<template>
  <!-- App.vue -->

  <v-app>
    <Head></Head>

    <!-- Sizes your content based upon application components -->
    <v-main>
      main<!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
import Head from './components/Head.vue'
export default {
  data() {
    return {
      tab: null,
      items: ['Appetizers', 'Entrees'],
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  },
  components: { Head }
}
</script>
<style lang="less" scoped>
/* Helper classes */
.basil {
  background-color: #fffbe6 !important;
}
.basil--text {
  color: #356859 !important;
  margin: 0 auto;
}
</style>
