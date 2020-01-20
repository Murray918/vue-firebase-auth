<template>
  <div class="login">
    <h3>Sign In</h3>
    <input type="text" placeholder="Email" />
    <input type="password" placeholder="Password" />
    <button>Connection</button>
    <p>you dont have an account ? you can create one</p>
  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    return {};
  },
  methods: {}
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
