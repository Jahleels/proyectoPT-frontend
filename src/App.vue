<template>
  <v-app>
    <header
      v-show="!['Admin', 'Usuarios', 'Consultantes'].includes($route.name)"
    >
      <the-navigation />
    </header>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import TheNavigation from "./components/TheNavigation.vue";

export default {
  components: { TheNavigation },
  name: "App",

  data: () => ({
    //
  }),
};
</script>
