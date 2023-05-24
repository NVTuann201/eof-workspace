<template>
  <v-container class="main fill-height pa-3 flex-column">
    <v-layout class="recent-workspace flex-column">
      <v-container>
        <div>Recent workspaces</div>
      </v-container>
      <v-layout>
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div>
        </v-card>
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div>
        </v-card>
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div>
        </v-card>
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div></v-card
        >
      </v-layout>
    </v-layout>
    <v-layout class="all-workspace flex-column">
      <v-container class="d-flex flex-row">
        <div class="ma-2">Order By</div>
        <div class="ma-2">Date</div>
        <div class="ma-2">Name</div>
        <div class="ma-2">Size</div>
        <v-spacer></v-spacer>
        <v-text-field single-line></v-text-field>
      </v-container>
      <v-layout>
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div></v-card
        >
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div></v-card
        >
        <v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div></v-card
        ><v-card class="card">
          <div class="card-info">Name1</div>
          <div class="date">date1</div>
          <div class="items-count">20 items</div>
          <div class="owner">Owner: Owner</div>
          <div class="size">Size: 400MB</div></v-card
        >
      </v-layout>
    </v-layout>
  </v-container>
</template>

<script setup>
import axios from "axios";
</script>
<script>
export default {
  name: "HelloWorld",
  data: () => ({
    workspaces: [],
  }),
  methods: {
    getWorkspaces() {
      axios
        .get("https://api-aws.eofactory.ai/api/workspaces?region=sea")
        .then((response) => {
          this.workspaces = response.data;
        });
    },
  },
  mounted() {
    this.workspaces = this.getWorkspaces();
  },
};
</script>
<style scoped>
.recent-workspace {
  margin: 28px 4px 4px 4px;
  width: 100%;
  flex-wrap: wrap;
}
.all-workspace {
  flex-wrap: wrap;
  width: 100%;
  margin: 56px 4px 4px 4px;
}
.main {
  width: 100% !important;
}
.card {
  width: 300px;
  height: 200px;
  margin: 4px;
  display: flex;
  flex-direction: column;
  padding: 12px 16px 0;
}
.v-text-field {
  max-width: 300px;
}
</style>
