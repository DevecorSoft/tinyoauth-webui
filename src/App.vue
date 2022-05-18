<script setup>
import { RouterView } from "vue-router";
import { DeHeader } from "@devecorsoft/devecorui";
import "@devecorsoft/devecorui/dist/style.css";
</script>

<template>
  <el-container>
    <el-header>
      <de-header :items="[]" title="tinyoauth" />
    </el-header>
    <el-main>
      <RouterView />
    </el-main>
  </el-container>
</template>
