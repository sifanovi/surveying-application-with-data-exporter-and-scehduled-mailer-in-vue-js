<template>
  <div class="container" id="app">
    <b-navbar variant="faded" type="light">
      <b-navbar-brand href="#">
        <img src="./assets/images/saxmundham_logo.jpg" class="nav-logo" alt="Kitten">
      </b-navbar-brand>
      <b-navbar-nav class="ml-auto">
        <b-navbar-brand href="#">
          <img src="./assets/images/smartMed.png" class="nav-logo" alt="Kitten">
        </b-navbar-brand>
      </b-navbar-nav>
    </b-navbar>
    <!-- ROUTER VIEW -->
    <router-view/>
    <!-- ROUTER VIEW -->
    <div>
      <b-navbar variant="faded" type="light" class="pb-5 pt-5 justify-content-center">
        <small>&copy; SmartMed Technologies Ltd 2020.  All rights reserved. </small>
      </b-navbar>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .nav-logo{
    height: 50px;
  }
</style>
