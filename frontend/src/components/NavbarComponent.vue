<template>
<div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">NavBar</b-navbar-brand>
  
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
  
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#"><router-link to="/">{{ $t('navbar.home') }}</router-link></b-nav-item>
          <b-nav-item href="#"><router-link to="/about">{{ $t('navbar.about') }}</router-link></b-nav-item>
          <b-nav-item href="#"><router-link to="/users">{{ $t('navbar.userList') }}</router-link></b-nav-item>
          <b-nav-item href="#"><router-link to="/um">{{ $t('navbar.userManagement') }}</router-link></b-nav-item>
        </b-navbar-nav>
  
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>
  
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>
  
          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>User</em>
            </template>
            <b-dropdown-item href="#">Profil</b-dropdown-item>
            <b-dropdown-item href="#"><router-link to="/login">Zaloguj się</router-link></b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
  <p>TEST</p>
  <a href="/about">{{ $t('navbar.about') }}</a>
</template>

<script>
export default {
    name: "NavbarComponent"
};
</script>



            
            
