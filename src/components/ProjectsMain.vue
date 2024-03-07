<template>
    <div class="wrapper">
      <div class="h2-cont">
        <h2 id="projects" class="projects">Projects</h2>
      </div>
  
      <div class="image-container-main">
        <img src="@/assets/white-place-holder.jpg" alt="Image 1">
        <img src="@/assets/white-place-holder.jpg" alt="Image 1">
        <img src="@/assets/white-place-holder.jpg" alt="Image 1">
        <img src="@/assets/white-place-holder.jpg" alt="Image 1">
        <img src="@/assets/white-place-holder.jpg" alt="Image 1">
        <img src="@/assets/white-place-holder.jpg" alt="Image 1">
    </div>

    <h2 class="tech"> Tech Stack </h2>
    <div class="image-container-tech">
        <img src="@/assets/css-3.png" alt="css">
        <img src="@/assets/java.png" alt="java">
        <img src="@/assets/java-script.png" alt="javascript">
        <img src="@/assets/html.png" alt="html">
        <img src="@/assets/python.png" alt="python">
        <img src="@/assets/sql-server.png" alt="sql">
        <img src="@/assets/git.png" alt="git">
        <img src="@/assets/github.png" alt="github">
    </div>

    </div>
  </template>
  
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
    width: 80%;
    justify-content: center;
    text-align: center;
    flex-wrap: wrap;
  }
  
  .image-container-main img {
    max-width: 50%;
    width: 25%;
    margin: 2%;
    border-radius: 10%;
  }
  
  .image-container-main img:hover {
    transform: scale(1.05);
    cursor: pointer;
    filter: blur(1px);
    -webkit-filter: blur(1px);
  }
  
  @media (max-width: 1100px) {
    .image-container-main img {
      max-width: 42%;
      width: 100%;
    }

    }
  
  @media (max-width: 600px) {

    .image-container-main img {
      max-width: 70%;
      width: 100%;
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
  