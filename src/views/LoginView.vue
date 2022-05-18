<script setup>
import { ref } from "vue";
import axios from "axios";
const username = ref("");
const password = ref("");
function login() {
  axios
    .post("/login", {
      username: username.value,
      password: password.value,
    })
    .then((res) => {
      console.log(res);
    });
}
</script>

<template>
  <div
    style="
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    "
  >
    <el-card style="width: 400px; height: 300px">
      <div>
        <p>User name</p>
        <el-input v-model="username" placeholder="username" clearable />
        <p>Password</p>
        <el-input
          v-model="password"
          placeholder="password"
          type="password"
          show-password
          clearable
        />
        <div style="height: 1rem"></div>
        <el-button type="primary" @click="login">Login</el-button>
      </div>
    </el-card>
    <el-card style="width: 400px; margin-top: 10px;">
      <div>New to tinyoauth? <el-link :underline="false" type="primary" href="/register">Create an account</el-link></div>
    </el-card>
  </div>
</template>
