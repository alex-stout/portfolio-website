<template>
  <Module id="contact">
    <v-container fluid>
      <v-layout justify-center>
        <v-flex md1 xs2 v-for="icon in icons" :key="icon.url">
          <a :href="icon.url">
            <v-icon large :color="icon.color" :class="icon.class">{{icon.text}}</v-icon>
          </a>
        </v-flex>
      </v-layout>
    </v-container>
  </Module>
</template>

<script>
import Module from "@/components/layout/Module";
export default {
  components: {
    Module
  },
  data() {
    return {
      icons: [
        {
          url: "https://linkedin.com/in/taylor-misch",
          class: "fab fa-linkedin fa-2x",
          text: "linkedin-box",
          color: "blue lighten-1"
        },
        {
          url: "https://github.com/taylor-misch",
          class: "fab fa-github",
          text: "github-box",
          color: "amber lighten-1"
        },
        {
          url: "mailto:taylormisch@gmail.com",
          class: "",
          text: "email",
          color: "red lighten-1"
        }
      ]
    };
  }
};
</script>

<style scoped>
a {
  text-decoration: none;
}
</style>
