<template>
  <v-app-bar>
    <v-app-bar-title>
      <v-layout class="header">
        <div class="logo">
          <v-img
            src="https://cdn.eofactory.ai/unsafe/0x45/https://eofactory.ai/images/logo/EOfactory-logo.png?ver=1.0.0"
          />
        </div>

        <v-layout class="header-content">
          <v-text-field
            density="compact"
            hide-details
            single-line
            variant="solo"
            prepend-inner-icon="mdi-magnify"
          ></v-text-field>
          <div class="pa-2">EOToken: 250</div>
          <div>
            <v-btn icon="mdi-help-circle-outline"></v-btn>
            <v-btn icon="mdi-bell-outline"></v-btn>
          </div>
          <v-select density="compact" variant="solo" hide-details></v-select>
          <div class="pa-2">
            <v-layout>
              <v-icon>mdi-account</v-icon>
              <span>NVTuann</span>
            </v-layout>
          </div>
        </v-layout>
      </v-layout>
    </v-app-bar-title>
  </v-app-bar>
</template>

<script setup>
//
</script>
<style scoped>
.logo {
  height: 60px;
  width: 120px;
  margin-right: 10px;
}
.header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  width: 100% !important;
}
.v-text-field {
  max-width: 450px !important;
}
.v-select {
  max-width: 150px !important;
}
.header-content{
  max-width: 1200px;
  justify-content: space-between;
}
</style>
