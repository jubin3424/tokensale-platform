<template>
  <div>
    <div style="background-color: #fff; height: 150vh; padding-top: 20px; border-top: 1px solid #d6dce5">
      <el-row>
        <el-col :xs="1" :sm="2">&nbsp;</el-col>
        <el-col :xs="22" :sm="20">
          <div>
            <el-dropdown>
                <span class="el-dropdown-link" style="font-size: 1rem;">
                  JbCoin
                </span>
              <el-dropdown-menu slot="dropdown">
                <el-dropdown-item>View All</el-dropdown-item>
              </el-dropdown-menu>
            </el-dropdown>
          </div>
        </el-col>
        <el-col :xs="1" :sm="2"></el-col>
      </el-row>
      <div class="b3">
  <el-row>
    <el-col :xs="1" :sm="2">&nbsp;</el-col>
    <el-col :xs="22" :sm="20">
      <div class="card-container">
        <el-row :gutter="30">
          <el-col :xs="24" :sm="12">
            <div style="position: relative;">
              <img src="../../static/coin/jbcoin.png" class="coin-image">
              <div class="coin-image-text" style="color: white">
                <h1 style="text-align: center;">Alphacon</h1>
                <el-button style="background-color: transparent; font-size: 1.5rem; padding: 1rem 1.5rem; color: white;">
                  <a href="https://alphacon.io/" style="color: white;">공홈 구매 바로가기</a></el-button>
              </div>
            </div>
          </el-col>
          <el-col :xs="24" :sm="12">
            <div class="coin-info">
              <div class="coin-info-detail">
                <b>Healthcare data platform</b> that acquires biometric data and provides quality personalized health solutions<br>
                <div class="coin-info-detail-indetail">
                  <table>
                    <tr>
                      <td class="table-header">Date</td><td class="table-content">2018. 7. 27 ~ 7. 30</td>
                    </tr>
                    <tr>
                      <td class="table-header">Price</td><td class="table-content">1 JBC = 0.5 PRST</td>
                    </tr>
                    <tr>
                      <td class="table-header">Bonus</td><td class="table-content">1% (1 JBC = 0.1 PRST)</td>
                    </tr>
                    <tr>
                      <td class="table-header">Platform</td><td class="table-content">ERC20</td>
                    </tr>
                    <tr>
                      <td class="table-header">SoftCap</td><td class="table-content">5,000 ETH</td>
                    </tr>
                    <tr>
                      <td class="table-header">HardCap</td><td class="table-content">37,500 ETH</td>
                    </tr>
                  </table>
                  <hr>
                  <table>
                    <tr>
                      <td class="table-header">HomePage</td><td class="table-content"
                    ><a href="https://presto-platform.io/"><i class="fas fa-home"></i></a></td>
                    </tr>
                    <tr>
                      <td class="table-header">WhitePaper</td><td class="table-content">
                      &nbsp;<a href="https://presto-platform.io/presto_whitepaper_en.pdf"><i class="fas fa-file-alt"></i></a></td>
                    </tr>
                  </table>
                </div>
              </div>
            </div>
          </el-col>
        </el-row>
      </div>
    </el-col>
    <el-col :xs="1" :sm="2">&nbsp;</el-col>
  </el-row>
      </div>
      <div style="border-bottom: 1px solid #d6dce5">
        <el-row>
          <el-col :xs="1" :sm="2">&nbsp;</el-col>
          <el-col :xs="22" :sm="20" class="information-tab">
            <span style="margin-right: 1.5rem; cursor: pointer;" @click="showCoinInfo" v-bind:class="{ active: selected === 'sebu' }">DAICO 세부정보</span>
            <span @click="showQuestion" style="cursor: pointer;" v-bind:class="{ active: selected === 'question' }">문의사항</span>
          </el-col>
          <el-col :xs="1" :sm="2">&nbsp;</el-col>
        </el-row>
      </div>
      <div style="text-align: center;">
        <el-row>
          <el-col :xs="1" :sm="2">&nbsp;</el-col>
          <el-col :xs="22" :sm="20" class="information-tab">
            <img v-if="isShow" src="../../static/coin/jbcontent.png">
            <img v-if="isQuestion" src="../../static/coin/quest.png" style="width: 80%; margin: auto;">
          </el-col>
          <el-col :xs="1" :sm="2">&nbsp;</el-col>
        </el-row>
      </div>
    </div>
  </div>
</template>

<script>
  import Parallax from 'vue-parallaxy'
  export default {
    name: 'JbCoin',
    data () {
      return {
        isShow: true,
        isQuestion: false,
        selected: 'sebu'
      }
    },
    methods: {
      showCoinInfo () {
        this.isShow = true
        this.isQuestion = false
        this.selected = 'sebu'
      },
      showQuestion () {
        this.isShow = false
        this.isQuestion = true
        this.selected = 'question'
      }
    },
    components: {
      Parallax
    }
  }
</script>

<style>
  .Masthead {
    height: 10vh !important;
    min-height: 10vh !important;
  }
  .b3 {
    background-color: #d6dce5;
    margin-top:15px;
    height: 65vh;
  }
  .b1 {
    background-color: pink;
  }
  .card-container {
    margin-top: 3rem;
  }
  img.image {
    width: 100%;
    height: 210px;
  }
  .el-card {
    margin-bottom: 6vh;
  }
  a {
    text-decoration: none;
    color: #333333;
  }
  .coin-image {
    width: 100%;
    height: 400px;
  }
  .coin-image-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .coin-info {
    background-color: white;
    height: 400px;
  }
  .coin-info-detail {
    padding: 2rem;
    word-break: break-all;
    font-size: 1.2rem;
  }
  .coin-info-detail-indetail {
    margin-top: 3rem;
  }
  table {
    font-size: 1rem;
  }
  .table-header {
    color: #7f7f7f;
  }
  .table-content {
    padding-left: 1rem;
    color: #222222;
  }
  .information-tab {
    padding: 1rem 0;
  }
  .active {
    color: #006666;
    font-weight: bolder;
  }
</style>
