<template>
  <nav id="navBar" class="" :class="{ sticky: active }">
    <div>
      <img
        :src="image"
        alt="Company Logo"
        class="img-fluid twoGutter"
        id="logo"
        v-scroll-to="{ el: '#navBar' }"
      />
    </div>

    <div id="navMenu">
      <span class="menuOption" v-scroll-to="{ el: '#navBar' }">HOME</span>
      <span
        class="menuOption activeMenuOption"
        v-scroll-to="{ el: '#aboutMeRow' }"
        >ABOUT</span
      >
      <span class="menuOption" v-scroll-to="{ el: '#querySection' }"
        >CONTACT</span
      >
    </div>
  </nav>
</template>

<script>
import logo from "../../images/logo.png";

export default {
  data() {
    return {
      image: logo,
      active: false
    };
  },

  methods: {
    toggleNavClass() {
      if (this.active == false) {
        return "navBar";
      } else {
        return "sticky-nav";
      }
    }
  },
  mounted() {
    window.document.onscroll = () => {
      let navBar = document.getElementById("navBar");
      if (window.scrollY > navBar.offsetTop) {
        this.active = true;
      } else {
        this.active = false;
      }
    };
  }
};
</script>
