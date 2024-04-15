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
    <div class="menu-web-mobile px-3">
      <div class="logo-web">
        <b-img src="@/assets/images/image_logo_Dsoft.png" width="" alt="big-logo" class="" />
      </div>
      <div class="button-menu">
        <b-icon icon="list" font-scale="2" v-b-toggle.sidebar-right></b-icon>
        <div class="menu-web">
          <b-sidebar id="sidebar-right" right shadow>
            <div class="px-3 py-2">
              <div class="item-menu">
                <span>Home</span>
              </div>
              <div class="item-menu">
                <span>Page</span>
              </div>
              <div class="item-menu">
                <span>Couse</span>
              </div>
              <div class="item-menu">
                <span>Feature</span>
              </div>
              <div class="item-menu">
                <span>Blog</span>
              </div>
              <div class="item-menu">
                <span>Shop</span>
              </div>
              <div class="item-menu muti-language">
                <b-img src="@/assets/images/ava-account.png" alt="big-logo" class="avatar-user" />
                <b-navbar-nav class="mx-auto color-black">
                  <b-nav-item-dropdown text="Home" right>
                    <b-dropdown-item href="#">EN</b-dropdown-item>
                    <b-dropdown-item href="#">ES</b-dropdown-item>
                    <b-dropdown-item href="#">RU</b-dropdown-item>
                    <b-dropdown-item href="#">FA</b-dropdown-item>
                  </b-nav-item-dropdown>
                </b-navbar-nav>
              </div>
            </div>
          </b-sidebar>
        </div>
      </div>
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