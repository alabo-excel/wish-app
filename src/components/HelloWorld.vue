<template>
  <v-container>
    <v-row class="text-center" justify="center">
      <v-col cols="10">
        <v-text-field label="Wish title" v-model="wishTitle"></v-text-field>
        <v-textarea
          outlined
          name="input-7-4"
          label="Enter your wish"
          v-model="wish"
        ></v-textarea>
      </v-col>
      <v-col cols="10">
        <v-card id="output" class="mx-auto mt-1" max-width="500" outlined>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="overline mb-4">Best Wishes</div>
              <v-list-item-title class="headline mb-1">
                {{ this.wishTitle }}
              </v-list-item-title>
              <v-list-item-subtitle>{{ this.wish }}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-divider></v-divider>
          <div class="text-center mt-3 p-5">
            <p>Powered By Wish</p>
          </div>
        </v-card>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4 mt-3 teal--text" icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      wish: "on your special day i wish you gods blessings and prosperity",
      wishTitle: "Happy birthday",
      icons: ["mdi-facebook", "mdi-twitter", "mdi-whatsapp", "mdi-instagram"],
    };
  },
  methods: {
    shareToFacebook() {
      var output = document.getElementById('output')
      let shareUrl = `http://www.facebook.com/sharer/sharer.phpu=${output}`;
      window.open(shareUrl, "NewWindow", );
    },
  },
};
</script>
<style></style>
