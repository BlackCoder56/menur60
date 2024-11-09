<template>
  <nav>
    <div class="nav-center">
      <!-- Logo on the left side -->
      <router-link to="/" class="logo">
        <img src="@/assets/brandlogo/menur4.png" alt="Logo" />
      </router-link>

      <!-- Centered Navbar Links -->
      <div class="nav-links">
        <router-link to="/">Home</router-link>

        <!-- About Us Dropdown with Active Link -->
        <div class="dropdown">
          <span 
            class="dropdown-link" 
            :class="{ active: isAboutActive }"
          >About Us</span> <!-- Dropdown trigger -->
          <div class="dropdown-content">
            <router-link to="/about">About Us</router-link>
            <router-link to="/objectives">Objectives</router-link>
            <router-link to="/values">Our Values</router-link>
          </div>
        </div>

        <router-link to="/news">News</router-link>
        <router-link to="/contact">Contact</router-link>
      </div>
    </div>
  </nav>
  
  <div class="content">
    <router-view/>
  </div>
</template>

<script>
import { computed } from "vue";
import { useRoute } from "vue-router";

export default {
  setup() {
    const route = useRoute();

    // Check if the current route is within the About Us section
    const isAboutActive = computed(() => {
      return ["/about", "/objectives", "/values"].includes(route.path);
    });

    return {
      isAboutActive,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #008080;
}

nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 15px 0;
  display: flex;
  justify-content: center; /* Center the nav-center container */
  z-index: 1000;
  transition: background-color 0.3s ease;
}

/* Center wrapper for logo and links */
.nav-center {
  display: flex;
  align-items: center;
  gap: 250px; /* Increased gap between logo and links */
}

/* Style for links in the nav-links container */
.nav-links {
  display: flex;
  gap: 15px; /* Space between nav links */
}

nav a {
  font-weight: bold;
  color: #008080; /* Teal color for links */
  text-decoration: none;
  transition: color 0.3s ease;
  font-size: 18px;
}

nav a.router-link-exact-active {
  color: #A67F59; /* Green color for active links */
  text-decoration: underline;
}

/* Logo styling */
.logo img {
  height: 40px; /* Adjust logo size */
  width: auto;
  margin-right: 50px; /* Additional spacing between logo and links */
}

/* Active Class for Dropdown Link */
.active {
  color: #A67F59;
  text-decoration: underline;
}

/* Dropdown Menu Styling */
.dropdown {
  position: relative;
}

.dropdown-link {
  cursor: pointer;
  font-weight: bold;
  color: #008080;
  font-size: 18px;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: rgba(255, 255, 255, 0.95);
  min-width: 150px;
  box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
  z-index: 1;
  border-radius: 5px;
}

.dropdown-content a {
  color: #008080;
  padding: 10px 15px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {
  background-color: #008080;
  color: white;
  border-radius: 5px;
}

.dropdown:hover .dropdown-content {
  display: block;
}

/* Content section below navbar */
.content {
  padding-top: 80px; /* Adjust based on the height of the fixed navbar */
}
</style>
