<script setup>
import { ref } from "vue";
const username = ref("");
const password = ref("");
</script>

<template>
  <el-input v-model="username" placeholder="username" clearable />
  <el-input
    v-model="password"
    placeholder="password"
    type="password"
    show-password
    clearable
  />
  <el-button type="primary" @click="login">Login</el-button>
</template>
