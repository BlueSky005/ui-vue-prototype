<template>
  <div id="app">
    <div class="content"></div>

    <Header />

    <HeroImgBanner />

    <CompanyStatistics />

    <AboutMe />

    <NeedAProject />

    <Footer />
  </div>
</template>

<script>
import Header from "./components/shared/Header";
import Footer from "./components/shared/Footer";
import AboutMe from "./components/AboutMe";
import CompanyStatistics from "./components/CompanyStatistics";
import HeroImgBanner from "./components/HeroImgBanner";
import NeedAProject from "./components/NeedAProject";
import "./css/main.css";
import "../css/bootstrap.lux.min.css";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    AboutMe,
    CompanyStatistics,
    HeroImgBanner,
    NeedAProject
  }
};
</script>

<style>
</style>