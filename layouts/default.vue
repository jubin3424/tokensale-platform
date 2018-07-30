<template>
  <div>
    <div id="app">
      <el-row>
        <el-col :span="2" class="navbar-box">
          &nbsp;
        </el-col>
        <el-col :span="5" class="navbar-box">
          <nuxt-link :to="{name: 'index'}">
            <img src="../static/img/logo.png" alt="" class="navbar__logo">
          </nuxt-link>
        </el-col>
        <el-col :span="17" class="navbar-box">
          <ul class="el-menu el-menu--horizontal navbar__menu">
            <li class="el-menu-item">DAICO?</li>
            <li class="el-menu-item">DAICO SVC</li>
            <li class="el-menu-item"><nuxt-link :to="{name: 'TokenSale'}">TokenSale</nuxt-link></li>
            <li class="el-menu-item">Airdrop</li>
            <li class="el-menu-item">Wallet</li>
          </ul>
        </el-col>
      </el-row>
      <nuxt/>
    </div>
  </div>
</template>

<style>
  #app {
    font-family: 'Raleway', Helvetica, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /*text-align: center;*/
  }
  /* latin */
  @font-face {
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 300;
    src: local('Raleway Light'), local('Raleway-Light'), url('../static/font/1Ptrg8zYS_SKggPNwIYqWqZPAA.woff2') format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }
  /* latin */
  @font-face {
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 400;
    src: local('Raleway'), local('Raleway-Regular'), url('../static/font/1Ptug8zYS_SKggPNyC0ITw.woff2') format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }
  /* latin */
  @font-face {
    font-family: 'Raleway';
    font-style: normal;
    font-weight: 600;
    src: local('Raleway SemiBold'), local('Raleway-SemiBold'), url('../static/font/1Ptrg8zYS_SKggPNwPIsWqZPAA.woff2') format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
  }
  body {
    margin: 0;
  }
  .navbar-box {
    height: 120px;
    background-color: #333f50;
  }
  .navbar__logo {
    height: 70px;
    display: block;
    margin-top: 24px;
    margin-left: auto;
    margin-right: auto;
  }
  .navbar__menu {
    margin-top: 30px;
    margin-right: 5%;
    float: right;
    background-color: #333f50;
  }
  .navbar__dropdown-menu a {
    color: inherit;
    text-decoration: none;
  }
  .el-menu--horizontal {
    border-bottom: solid 1px #333f50;
  }
  .el-menu--horizontal > .el-menu-item {
    color: #FFFFFF;
    font-weight: bold;
  }
  .el-menu--horizontal > .el-menu-item:not(.is-disabled):hover {
    background-color: #333f50;
    color: #006666;
    font-weight: bold;
  }
</style>

