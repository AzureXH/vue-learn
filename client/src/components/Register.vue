<template>
  <div>
    <h1>Register</h1>
    <input type="email" name="email" placeholder="email" v-model="email" />
    <br />
    <input
      type="password"
      name="password"
      placeholder="password"
      v-model="password"
    />
    <br />
    <button @click="register">Register</button>
  </div>
</template>

<script>
import AuthenticationService from "@/services/AuthenticationService";
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
  watch: {
    email(value) {
      console.log("email has change", value);
    },
  },
  methods: {
    async register() {
      await AuthenticationService.register({
        email:this.email,
        password:this.password
      })
    },
  },
  mounted() {
    setTimeout(() => {
      this.email = "hello world";
    }, 2000);
  },
};
</script>

<style scoped>
</style>
