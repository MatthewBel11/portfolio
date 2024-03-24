<template>
    <div class="wrapper">
      <div class="h2-cont">
        <h2 id="projects" class="projects">Projects</h2>
      </div>
  
      <div class="image-container-main">

        <div class="item">
          <img src="@/assets/Capture.png">
          <img class="hover-image" src="@/assets/white-place-holder.jpg">
          <p class="paragraph-1">The WineDataProject analyzes wine quality and characteristics using Python, uncovering insights through visualization and machine learning techniques.</p>
        </div>

        <div class="item">
          <a href="https://github.com/MatthewBel11/WineDataProject">
            <img src="@/assets/white-place-holder.jpg" alt="Image 1">
          </a>
        </div>

        <div class="item">
          <a href="https://github.com/MatthewBel11/WineDataProject">
            <img src="@/assets/white-place-holder.jpg" alt="Image 1">
          </a>
        </div>

        <div v-show="screenWidth > 670" class="item">
          <a href="https://github.com/MatthewBel11/WineDataProject">
            <img src="@/assets/white-place-holder.jpg" alt="Image 1">
          </a>
        </div>

        <div v-show="screenWidth > 670" class="item">
          <a href="https://github.com/MatthewBel11/WineDataProject">
            <img src="@/assets/white-place-holder.jpg" alt="Image 1">
          </a>
        </div>

        <div v-show="screenWidth > 670" class="item">
          <a href="https://github.com/MatthewBel11/WineDataProject">
            <img src="@/assets/white-place-holder.jpg" alt="Image 1">
          </a>
        </div>
    </div>

    <h2 class="tech"> Tech Stack </h2>
    <div class="image-container-tech">
        <img src="@/assets/css-3-c.png" alt="css">
        <img src="@/assets/java-c.png" alt="java">
        <img src="@/assets/java-script-c.png" alt="javascript">
        <img src="@/assets/html-c.png" alt="html">
        <img src="@/assets/python-c.png" alt="python">
        <img src="@/assets/sql-server-c.png" alt="sql">
        <img src="@/assets/c-sharp.png" alt="git">
        <img src="@/assets/github-c.png" alt="github">
    </div>

    </div>
  </template>

<script>
import { ref, onMounted, onUnmounted } from 'vue';

export default {
  setup() {
    const screenWidth = ref(window.innerWidth);

    const check = () => {
      screenWidth.value = window.innerWidth;
      // Do something with screenWidth if needed
    };

    onMounted(() => {
      check();
      document.title = "Matthew's Portfolio";

      // Add event listener on mount
      window.addEventListener('resize', check);
    });

    onUnmounted(() => {
      // Remove event listener on unmount
      window.removeEventListener('resize', check);
    });

    return {
      screenWidth
    };
  },
};
</script>


  
  <style scoped>

  .wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .h2-cont {
    width: 100%;
  }
  
  .projects,
  .tech {
    color: azure;
    text-align: center;
  }
  
  .image-container-main {
    margin: 0 auto;
    padding: 0;
    display: flex;
    flex-direction: row;
    width: 60%;
    justify-content: center;
    text-align: center;
    flex-wrap: wrap;
  }
  
  .item {
    position: relative;
    width: 30%;
    margin: 10px;
    margin-bottom: 50px;
    overflow: hidden;
  }

  .item img {
    max-width: 100%;
    border-radius: 10%;
    transition: opacity 0.3s ease; /* Add transition effect for smooth hover */
  }

  .item .hover-image {
    display: none; /* Initially hide the hover image */
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
  }

  .item:hover .hover-image {
    display: block; /* Show the hover image on hover */
  }

  .item:hover img {
    opacity: 0; /* Hide the original image on hover */
  }

  .paragraph-1{
    font-size: 0.8vw;
    width: 80%;
  }

  .item .paragraph-1 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -75%);
    color: rgb(255, 255, 255);
    font-family: Arial, sans-serif;
    display: none;
    z-index: 2; /* Ensure the paragraph appears above the hover image */
    transition: opacity 0.3s ease; /* Add transition effect for smooth hover */
  }

  .item:hover .paragraph-1 {
    display: block; /* Show the paragraph on hover */
    opacity: 1; /* Make the paragraph fully visible */
  }
  
  @media (max-width: 1100px) {

    .item{
      width: 45%;
      margin-bottom: 20px;
    }

    .paragraph-1{
      font-size: 1.5vw;
    }

    .item img {
      width: 100%;
    }

    }
  
  @media (max-width: 670px) {

    .item{
      width: 100%;
      margin-bottom: 20px;
    }

    .item img {
      width: 100%;
    }

    .paragraph-1{
      font-size: 3vw;
    }

    }
  
  .tech {
    margin-top: 1%;
  }
  
  .image-container-tech {
    display: flex;
    width: 60%;
    margin: 0 auto;
    padding: 0;
    justify-content: center;
    margin-top: 1%;
    flex-wrap: wrap;
  }
  
  .image-container-tech img {
    width: 7.5%;
    margin-right: 1%;
    margin-left: 1%;
  }

  .image-container-tech img:hover{
    transform: scale(1.05);
  }

  @media (max-width: 1100px) {
    .image-container-tech img {
    min-width: 42px;
    width: 10%; /* Adjust the width to fit two images in a line */
    margin: 1%;  /* Add margin for spacing between images */
  } 
}


  @media (max-width: 600px) {
    .image-container-tech img {
    width: 12.5%; /* Adjust the width to fit two images in a line */
    margin: 1%;  /* Add margin for spacing between images */
  } 
}

    @media (max-width: 360px) {
    .projects{
        font-size: 120%;
    }

    .tech{
        font-size: 120%;
    }
    }

    

  </style>
  