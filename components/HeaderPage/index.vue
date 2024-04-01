<template>
  <div class="header w-100 fixed-top">
    <div class="menu-web-pc">
      <b-navbar type="light" variant="lights">
        <div style="width: 150px;">
          <b-img src="@/assets/images/image_logo_Dsoft.png" alt="big-logo" class="w-100" />
        </div>
        <b-navbar-nav class="mx-auto">
          <b-nav-item-dropdown text="Home" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <!-- Navbar dropdowns -->
          <b-nav-item-dropdown text="Page" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="Coues" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="Feature" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="Blog" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="Shop" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>

          <div class="icon-header">
            <div>
              <b-icon icon="search"></b-icon>
            </div>
            <div>
              <b-icon icon="cart2"></b-icon>
            </div>
          </div>
        </b-navbar-nav>
        <div class="info-account d-flex align-items-center">
          <b-img src="@/assets/images/ava-account.png" alt="big-logo" class="avatar-user" />
          <b-navbar-nav class="mx-auto">
            <b-nav-item-dropdown text="Home" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </div>
      </b-navbar>
    </div>
  </div>
</template>

<script>
import { BIcon, BIconArrowUp, BIconArrowDown } from 'bootstrap-vue'

export default {
  name: 'HeaderPage',
  components: {
    BIcon,
    BIconArrowUp,
    BIconArrowDown
  },
}
</script>
<style>
@import '~/assets/scss/header/header.scss';
@import 'bootstrap-vue/dist/bootstrap-vue-icons.min.css';
</style>