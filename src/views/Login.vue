<template>
  <div class="login">
    <h3>Sign In</h3>
    <input type="text" v-model="email" placeholder="Email" />
    <input type="password" v-model="password" placeholder="Password" />
    <button @click="login">Connection</button>
    <p>
      If you dont have an account ? you can
      <router-link to="/signup">create one </router-link>
    </p>
  </div>
</template>

<script>
import firebase from "firebase";

export default {
  name: "login",
  data() {
    return {};
  },
  methods: {
    login: async function() {
      try {
        console.log(this.email);
        console.log(this.password);
        const success = await firebase
          .auth()
          .signInWithEmailAndPassword(this.email, this.password);
        console.log(success.json());
        alert(`congrats ${this.email} you have successfully signed in`);
        this.$router.push("/home");
      } catch (error) {
        alert(error);
      }
    }
  }
};
</script>

<style scoped>
.login {
  display: flex;
  width: 100%;
  height: 100%;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

input {
  margin: 10px 0;
  width: 40%;
  padding: 15px;
}

button {
  margin-top: 10px;
  width: 15%;
  cursor: pointer;
}

p {
  margin-top: 40px;
  font-size: 13px;
}

p a {
  text-decoration: underline;
  cursor: pointer;
}
</style>
