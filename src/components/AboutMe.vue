<template>
  <div class="row g-0">
    <div id="aboutMeRow">
      <div class="" id="aboutMeLeft">
        <img
          :src="aboutMeImg"
          alt="About me left content"
          class="img-fluid animated fadeIn"
        />
      </div>
      <div class="" id="aboutMeRight">
        <div class="aboutMeContent">
          <h4 class="animated fadeIn" id="aboutMeCaption">About me</h4>

          <div class="txtContentColor">
            <p class="animated fadeIn">
              Given let waters air sea had you'll, may seed abundantly fish.
              Were, you'll earth forth winged above brought. Own darkness
              they're him can't fourth sea place have.
            </p>
            <p class="animated fadeIn">
              So the above May stars cattle fruitful face shall. Tree it,
              winged. Every signs male firmament us. Morning him.
            </p>
          </div>

          <img
            :src="signatureImg"
            alt="Signature"
            class="img-fluid animated fadeIn"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import aboutMeImg from "../images/about-me.png";
import signatureImg from "../images/signature-transparentbg.png";

export default {
  data() {
    return {
      aboutMeImg,
      signatureImg
    };
  }
};
</script>
