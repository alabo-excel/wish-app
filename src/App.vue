<template>
  <v-app>
    <v-app-bar app color="teal" dark>
      <img width="60" src="./assets/logo.png" alt="" />
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <HelloWorld />
    </v-main>
    <v-footer color="teal">
      <p class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>Alabo Excel</strong>
      </p>
      <v-spacer></v-spacer>
      <img width="60" src="./assets/logo.png" alt="" />
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
