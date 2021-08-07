<template>
  <div class="row g-0">
    <div id="overlayImg">
      <div id="overlayTxtSection">
        <div>
          <h2 class="headerTxtColor animated fadeIn">Amelia Woods</h2>
        </div>
        <div class="animated fadeInUp">
          I am a Graphic & Web Designer based in New York, specializing in User
          Interface Design and Development.
        </div>
      </div>
    </div>
    <img
      :src="headerAboutMeImg"
      alt="About Me"
      class="img-fluid aboutMeImg animated fadeIn"
      id="aboutMePic"
    />
  </div>
</template>

<script>
import headerAboutMeImg from "../images/header-about-me.png";

export default {
  data() {
    return {
      headerAboutMeImg
    };
  }
};
</script>
