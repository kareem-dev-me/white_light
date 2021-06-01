<template>
  <v-app>
    <v-main>
      <nuxt />
    </v-main>

    <v-footer :absolute="false" app>
      <a href="mailto:kareembasuonyg@gmail.com">Kareem</a> &nbsp;هذا الموقع صمم
      بواسطة
      <span> &copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>
