<template>
  <v-app dark>

    <v-app-bar
      fixed
      app
      elevation="0"
      class="white"
    >
      <v-toolbar-title>{{ title }}</v-toolbar-title>
      <v-spacer />
    </v-app-bar>
    <v-main>
      <div>
        <Nuxt />
      </div>
    </v-main>
    <v-footer
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
// import vue from "vue";
export default {
  name: 'DefaultLayout',
  data () {
    return {
      title: 'Class CW1 2019-2023'
    }
  }
}
</script>
