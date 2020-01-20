<template>
  <div class="sign-up">
    <input type="text" v-model="email" placeholder="Email" />
    <input type="password" v-model="password" placeholder="Password" />
    <button @click="signup">Sign In</button>
    <router-link to="/login">return to login</router-link>
  </div>
</template>

<script>
import firebase from "firebase";

export default {
  name: "Signup",
  data() {
    return {};
  },
  methods: {
    signup: async function(item) {
      console.log(item);
      try {
        const success = await firebase
          .auth()
          .createUserWithEmailAndPassword(this.email, this.password);
        console.log(success);
        alert(`success ${this.emial} your account has been created`);
        this.$router.push("/home");
      } catch (error) {
        alert(error.message);
      }
    }
  }
};
</script>

<style scoped>
.sign-up {
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

a {
  text-decoration: underline;
  cursor: pointer;
}
</style>
