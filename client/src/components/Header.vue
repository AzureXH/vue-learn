<template>
  <v-toolbar fixed class="cyan" dark>
    <v-toolbar-title class="mr-4">
      <span class="home" @click="navigateTo({ name: 'root' })">
        TabTracker
      </span>
    </v-toolbar-title>

    <!-- TODO: Implement Me -->
    <!-- <v-toolbar-items>
      <v-btn flat dark>Browse</v-btn>
    </v-toolbar-items> -->
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn flat dark class="cyan" @click="navigateTo({ name: 'login' })">
        Login
      </v-btn>
      <v-btn flat dark class="cyan" @click="navigateTo({ name: 'register' })">
        Sign Up
      </v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {
  name: "Header",
  methods: {
    navigateTo(route) {
      this.$router.push(route);
    },
  },
};
</script>

<style scoped>
.home {
  cursor: pointer;
}
.home:hover {
  color: #e9e;
}
</style>
