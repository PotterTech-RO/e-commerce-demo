<template>
  <div class="navbar">
    <div class="logo-section">
      <LogoComponent />
      <p class="company-name">PotterTech</p>
    </div>
    <div class="drawer">
      <v-icon icon="mdi-menu"></v-icon>
    </div>
    <div class="navbar-items">
      <span>Categories</span>
      <span>Deals</span>
      <span>What's New</span>
      <span>Delivery</span>
    </div>
    <v-responsive class="ml-auto" min-width="200" style="display: flex;">
      <v-text-field class="search-input" clearable append-inner-icon="mdi-magnify" hide-details="auto" density="compact"
        label="test" variant="outlined"></v-text-field>
    </v-responsive>
    <div class="navbar-items-right">
      <div>Account</div>
      <div>Cart</div>
    </div>
  </div>
</template>

<script setup>
import LogoComponent from './LogoComponent.vue'

</script>

<style scoped>
.navbar {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  /* gap: 6rem; */
  padding: 1rem 7rem;
  /* background-color: greenyellow; */
  width: 100%;
  height: 100%;
}

.navbar-items {
  display: flex;
  flex-direction: row;
  margin: 0rem 2rem;
  gap: 2rem;
  white-space: nowrap;
  font-weight: 600;
  font-size: 1rem;
}

.navbar-items-right {
  display: flex;
  flex-direction: row;
  gap: 2rem;
  margin-left: 2rem;
  font-size: 1rem;
  font-weight: 600;
}

.company-name {
  font-size: 1.6rem;
  font-weight: bolder;
}

.logo-section {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 1rem;
}

.drawer {
  display: none;
}

.search-input {
  /* height: 1rem; */
  /* margin-left: 4rem; */
  min-width: 2rem;
  max-width: 20rem;
}

@media (max-width: 1226px) {

  /* CSS styles for devices with width below 1126px */
  /* Add your styles here */
  .logo-section {
    display: none;
  }

  .navbar-items {
    margin: 0;
    margin-right: 2rem;
  }

}

@media (max-width: 986px) {

  /* CSS styles for devices with width below 1126px */
  /* Add your styles here */
  /* .logo-section {
    display: none;
  } */

  .navbar-items {
    display: none;
  }

  .drawer {
    display: initial;
    margin-right: 2rem;
  }

}
</style>
