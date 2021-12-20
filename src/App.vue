<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { reactive } from "vue";
import Tree from "vue3-treeview";
import "vue3-treeview/dist/style.css";

const treeNodes = reactive({
  id1: {
    text: "text1",
    children: ["id11", "id12"],
  },
  id11: {
    text: "text11",
    children: ["id112"],
  },
  id12: {
    text: "text12",
    children: ["id111"],
  },
  id111: {
    text: "text111",
  },
  id112: {
    text: "text111",
  },
});

const treeConfig = {
  roots: ["id1"],
};
</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <tree :config="treeConfig" :nodes="treeNodes"> </tree>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
