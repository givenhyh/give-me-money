<template>
  <div id="app">
    <el-container>
      <el-header>
        <navbar></navbar>
      </el-header>

      <el-main>
        <router-view />
      </el-main>

      <el-footer>
        <hr />
        <div>
          <a href="https://www.unicef.cn/" target="_blank">联合国儿童基金会</a>
        </div>
        <vue-about-me :copyright="copyright"></vue-about-me>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
import Navbar from "./components/common/Navbar";
import VueAboutMe from "vue-about-me";
export default {
  name: "App",
  components: {
    Navbar,
    VueAboutMe
  },
  data() {
    return {
      header: "可爱的萝莉妹妹们",
      msg: "欧尼酱，可以……告诉我……你的……支付宝吗？",
      copyright: {
        name: "Give Me Money!",
        repoName: "give-me-money",
        author: "YunYouJun",
        logo: "#icon-cloud"
      }
    };
  }
};
</script>

<style>
body {
  padding: 0;
  margin: 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
hr {
  opacity: 0.2;
}
.el-header {
  padding: 0 !important;
}
.el-main {
  padding: 0 0.5rem !important;
}
</style>
