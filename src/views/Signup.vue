<template>
  <div class="sign-up">
    <input type="text" placeholder="Email" />
    <input type="password" placeholder="Password" />
    <button>Sign In</button>
    <span>return to login</span>
  </div>
</template>

<script>
export default {
  name: "Signup",
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
