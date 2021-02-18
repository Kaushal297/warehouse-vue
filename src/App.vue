<template>
  <div id="app">
    <h1 class="text-align-center">ABC Logistics</h1>
    <div class="navigation">
      <router-link to="/">List </router-link>
      <router-link to="/details" class="m-b-5"> Details</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  line-height: 1.4;
}

.flex-jc-cntr {
  display: flex;
  justify-content: center;
}

.text-align-center {
  text-align: center;
}

.m-b-5 {
  margin-bottom: 50px;
}

.navigation {
  text-align: center;
  margin: 20px 0;
}

.navigation router-link {
  padding-right: 50px;
}
</style>
