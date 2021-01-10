<template>
  <div>
    <b-navbar type="dark" variant="dark">
      <b-navbar-nav>
        <b-nav-item href="#" class="judul">NewsToday</b-nav-item>
        <li>
          <router-link class="nav-link" to="/nasional">Nasional</router-link>
        </li>
        <li>
          <router-link class="nav-link" to="/internasional">Internasional</router-link>
        </li>


        <!-- Navbar dropdowns 
        <b-nav-item-dropdown text="Nasio" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">RU</b-dropdown-item>
          <b-dropdown-item href="#">FA</b-dropdown-item>
        </b-nav-item-dropdown>

        <b-nav-item-dropdown text="User" right>
          <b-dropdown-item href="#">Account</b-dropdown-item>
          <b-dropdown-item href="#">Settings</b-dropdown-item>
        </b-nav-item-dropdown>
-->
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
.judul {
  font-weight: bold;
}
</style>