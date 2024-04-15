<template>
  <div class="footer-web">
    <div class="body-footer row py-3">
      <div class="col-lg-3 col-sm-6"> 
          <h3 class="title">Company</h3>
          <div class="description d-flex flex-column">
            <span>About</span>
            <span>Careers</span>
            <span>Pross</span>
            <span>Blog</span>
            <span>Affiliates</span>
          </div>
      </div>
      <div class="col-lg-3 col-sm-6"> 
          <h3 class="title">Community</h3>
          <div class="description d-flex flex-column">
            <span>Go Premium</span>
            <span>Team Plans</span>
            <span>Refer a Friend</span>
            <span>Gift Cards</span>
            <span>Scholarships</span>
            <span>Free Classes</span>
          </div>
      </div>
      <div class="col-lg-3 col-sm-6"> 
          <h3 class="title">Company</h3>
          <div class="description d-flex flex-column">
            <span>Become a</span>
            <span>Teacher</span>
            <span>Teaching</span>
            <span>Academy</span>
            <span>Teacher</span>
            <span>Hand Book</span>
          </div>
      </div>
      <div class="col-lg-3 col-sm-6"> 
          <h3 class="title">Support</h3>
          <div class="description d-flex flex-column">
            <span>Support</span>
            <span>Contact Us</span>
            <span>System Requirements</span>
            <span>Register Activation</span>
            <span>Key</span>
            <span>Site Feedback</span>
          </div>
      </div>
    </div>
    <div class="footer d-flex justify-content-between align-items-center ali pt-3">
      <div class="text">
        © 2015-2020 Skillfy Education Private Limited. All rights reserved
      </div>
      <div class="icon-footer">
        <b-icon class="px-3" icon="facebook" font-scale="3"></b-icon>
        <b-icon class="px-3" icon="twitter" font-scale="3"></b-icon>
        <b-icon class="px-3" icon="google" font-scale="3"></b-icon>
        <b-icon class="px-3" icon="linkedin" font-scale="3"></b-icon>
      </div>
    </div>
  </div>
</template>

<script>
import { BIcon, BIconArrowUp, BIconArrowDown } from 'bootstrap-vue'

export default {
  name: 'FooterPage',
  components: {
    BIcon,
    BIconArrowUp,
    BIconArrowDown
  },
}
</script>
<style>
@import '~/assets/scss/footer/footer.scss';
@import 'bootstrap-vue/dist/bootstrap-vue-icons.min.css';
</style>