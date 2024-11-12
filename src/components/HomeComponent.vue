<template>
  <div class="homepage">
    <!-- Background image and overlay content -->
    <div class="background-image">
      <div class="overlay">
        <h1>Empowering Change for a Sustainable Future</h1>
        <p>Leading agricultural transformation, resilient livelihoods, and climate action for balanced ecosystems.</p>
        <router-link to="/about" class="button">Learn More</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePage",
};
</script>

<!-- Scoped CSS for the component -->
<style scoped>
/* Full-page background styling */
.homepage {
  height: 85vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f5f5f5; /* Light background color for fallback */
}

.background-image {
  position: relative;
  width: 100%;
  height: 113%;
  background-image: url("@/assets/homepage/background.jpg"); /* Replace with your image path */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

/* Overlay styling */
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 98%;
  height: 96%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 128, 128, 0.6); /* Teal overlay with transparency */
  color: #f5f5f5; /* Light text color */
  text-align: center;
  padding: 20px;
}

/* Heading and paragraph styles */
.overlay h1 {
  font-size: 3rem;
  color: #ffffff;
  margin-bottom: 10px;
}

.overlay p {
  font-size: 1.5rem;
  color: #e0e0e0;
  margin-bottom: 20px;
}

/* Button styling */
.button {
  display: inline-block;
  padding: 12px 25px;
  background-color: #4CAF50; /* Green button */
  color: #ffffff;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: #3b9d3b; /* Darker green on hover */
}
</style>
