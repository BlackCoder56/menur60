<template>
    <div class="about-page">
      <!-- Header -->
      <h1>About Menur 60<sup>o</sup></h1>
  
      <!-- Full-width image with 100vw -->
      <div class="about-image">
        <img src="@/assets/aboutpage/about-image1.jpg" alt="About Us Image" />
      </div>
  
      <!-- Three columns with content -->
      <div class="about-content">
        <div class="column">
          <h2>About Menure 60<sup>o</sup></h2>
          <p>
            <span class="drop-cap">E</span>mpowering communities through sustainable agriculture practices and climate action initiatives for a resilient future. We focus on providing resources, support, and knowledge to help communities achieve self-sufficiency and environmental balance. Our mission is to create impactful change that fosters long-term sustainability and provides tools for adapting to climate challenges. We partner with local leaders to implement best practices and make a meaningful impact.
          </p>
          <div class="read-more-container">
            <button @click="goToMissionPage" class="read-more">Read More</button>
          </div>
        </div>
        <div class="column">
          <h2>Our Vision</h2>
          <p>
            <span class="drop-cap">A</span> sustainable world where women and youth lead the transformation of agriculture and champion climate initiatives. We envision a future where empowered individuals collaborate to create resilient agricultural systems and advocate for a healthier planet. Through our programs, we aim to build communities that value biodiversity, adapt to climate shifts, and lead innovative, eco-friendly solutions.
          </p>
          <div class="read-more-container">
            <button @click="goToVisionPage" class="read-more">Read More</button>
          </div>
        </div>
        <div class="column">
          <h2>Our Values</h2>
          <p>
            <span class="drop-cap">I</span>ntegrity, resilience, and a commitment to environmental stewardship drive our actions and partnerships. We believe in accountability, transparency, and respect for nature and humanity. Our values shape our approach to building partnerships and engaging with communities, focusing on environmental preservation and social responsibility.
          </p>
          <div class="read-more-container">
            <button @click="goToValuesPage" class="read-more">Read More</button>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "AboutComponent",
    methods: {
      goToMissionPage() {
        this.$router.push("/mission");
      },
      goToVisionPage() {
        this.$router.push("/vision");
      },
      goToValuesPage() {
        this.$router.push("/values");
      },
    },
  };
  </script>
  
  <style scoped>
  /* Set full viewport height */
  .about-page {
    height: 96vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 20px;
    box-sizing: border-box;
    text-align: center;
    font-family: 'Georgia', 'Times New Roman', serif; /* Suitable for older age bracket */
  }
  
  /* Header styling */
  .about-page h1 {
    font-size: 2.5rem;
    color: #008080;
    margin: 0;
  }
  
  /* Full-width image styling with reduced margin */
  .about-image img {
    width: 96vw;
    height: 300px;
    object-fit: cover;
    margin: 10px 0 20px 0;
  }
  
  /* Content section with three columns */
  .about-content {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    width: 95%;
  }
  
  /* Individual column styling with left border */
  .column {
    flex: 1;
    padding: 20px;
    background-color: #f5f5f5;
    border-radius: 8px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    position: relative;
    text-align: justify;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .column::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 4px;
    height: 100%;
    background-color: #4CAF50;
    border-radius: 2px;
  }
  
  .column h2 {
    font-size: 1.5rem;
    color: #008080;
    margin-bottom: 10px;
  }
  
  .column p {
    font-size: 1.125rem; /* Slightly larger for readability */
    color: #333333;
    line-height: 1.6;
  }
  
  /* Drop cap styling */
  .drop-cap {
    font-size: 3rem; /* Increase the drop cap size for clarity */
    font-weight: bold;
    float: left;
    margin-right: 6px;
    color: #4CAF50;
    line-height: 1;
    vertical-align: top;
  }
  
  /* Read More button styling */
  .read-more-container {
    margin-top: 10px;
  }
  
  .read-more {
    background-color: #008080;
    color: #fff;
    border: none;
    padding: 8px 12px;
    cursor: pointer;
    border-radius: 4px;
    transition: background-color 0.3s;
    width: fit-content;
  }
  
  .read-more:hover {
    background-color: #006666;
  }
  </style>
  