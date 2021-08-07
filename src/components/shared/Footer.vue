<template>
  <footer class="footer">
    <div class="footerCompanyContainer">
      <h5 class="footerCompanyName">Piroll Design, Inc.</h5>
      <span class="copywriteInfo"
        >© <span> {{ currentYear }} </span> Piroll. All rights reserved.</span
      ><br />
      <span>Designed by robirurk.</span>
    </div>

    <div class="footerEmailContainer">
      <p class="footerEmailContent">
        hello@pirolltheme.com <br />
        +44 987 065 908
      </p>
    </div>

    <div class="workDetailsContainer">
      <div>Projects</div>
      <div>About</div>
      <div>Services</div>
      <div>Career</div>
    </div>

    <div class="actionOptions">
      <div>News</div>
      <div>Events</div>
      <div>Contact</div>
      <div>Legals</div>
    </div>

    <div class="socialMediaOptions">
      <div>Facebook</div>
      <div>Twitter</div>
      <div>Instagram</div>
      <div>Dribbble</div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear()
    };
  }
};
</script>


