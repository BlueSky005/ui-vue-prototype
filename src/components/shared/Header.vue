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
      <span
        :class="homeMenuStatus ? 'menuOption activeMenuOption' : 'menuOption'"
        v-scroll-to="{ el: '#navBar' }"
        @click="homeClicked"
        >HOME</span
      >
      <span
        :class="aboutMenuStatus ? 'menuOption activeMenuOption' : 'menuOption'"
        v-scroll-to="{ el: '#aboutMeRow' }"
        @click="aboutClicked"
        >ABOUT</span
      >
      <span
        :class="
          contactMenuStatus ? 'menuOption activeMenuOption' : 'menuOption'
        "
        v-scroll-to="{ el: '#querySection' }"
        @click="contactClicked"
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
      active: false,
      homeMenuStatus: true,
      aboutMenuStatus: false,
      contactMenuStatus: false
    };
  },

  methods: {
    toggleNavClass() {
      if (this.active == false) {
        return "navBar";
      } else {
        return "sticky-nav";
      }
    },

    homeClicked() {
      this.homeMenuStatus = true;
      this.aboutMenuStatus = false;
      this.contactMenuStatus = false;
    },

    aboutClicked() {
      this.aboutMenuStatus = true;
      this.homeMenuStatus = false;
      this.contactMenuStatus = false;
    },

    contactClicked() {
      this.aboutMenuStatus = false;
      this.homeMenuStatus = false;
      this.contactMenuStatus = true;
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
