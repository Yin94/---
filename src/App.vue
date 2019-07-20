<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/auth/1">Signin</router-link>|
      <router-link to="/auth/0">Signup</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
@import "~bootstrap/dist/css/bootstrap.min.css";
</style>
