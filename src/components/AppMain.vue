
<template>
  <div id="intro" class="wrapper">
    <div class="face">
      <img src="@/assets/face.png" alt="Matthew's face">
    </div>

    <div class="typing">
      <h1 class="matthew">Hey, I'm Matthew 👋</h1>
    </div>

    <h2 class="sub-main">A Junior Software Engineer 💻</h2>


    <div class="icons">
      <a href="https://www.linkedin.com/in/swematthew101/" class="social-link">
        <img src="@/assets/linkedin.png" alt="LinkedIn">
      </a>
      <a href="https://github.com/MatthewBel11?tab=overview&from=2023-12-01&to=2023-12-19" class="social-link">
        <img src="@/assets/github.png" alt="GitHub">
      </a>
      <a href="https://twitter.com/matthew_ncl" class="social-link">
        <img src="@/assets/twitter.png" alt="Twitter">
      </a>
    </div>

    <div class="sub-intro">
    <p class="intro">
      A University student with a passion for software engineering, aspiring to contribute my skills to innovative projects.
      Born, raised, and educated all within Newcastle Upon Tyne (The best city in the U.K). I currently work at Ikea, which means not only can I code, but I'm great with flat pack furniture!
    </p>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  height: 100vh;
  color: azure;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.face {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 25%;
  margin: 0 auto;
}

.face img {
  margin-top: 2%;
  border-radius: 50%;
  max-width: 100%;
  min-width: 150px;
}

.typing {
  display: inline-block;
}

.matthew {
  letter-spacing: 3px;
  overflow: hidden;
  border-right: 2.5px solid white;
  white-space: nowrap;
  width: 100%;
  animation: typing 2s steps(17),
    cursor .6s step-end infinite alternate;
}

@keyframes cursor {
  50% {
    border-color: transparent;
  }
}

@keyframes typing {
  from {
    width: 0;
  }
}

.sub-main {
  width: 100%;
  text-align: center;
}


.typing {
  display: inline-block;
}

.sub-intro {
  width: 100%;
  text-align: center;
}

.intro {
  margin: 0 auto;
  max-width: 50%; /* Adjust the maximum width as needed */
  word-wrap: break-word;
  text-align: center;
  line-height: 1.6;
}

.icons {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 1%;
}

.icons a {
  margin-left: 1.5%;
  margin-right: 1.5%;
  width: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.icons img {
  max-width: 100%;
  max-height: 100%;
  width: auto;
  height: auto;
}

@media screen and (max-width: 440px) {
  .matthew {
    font-size: 180%;
    margin-top: 15%;
  }

  .icons {
    max-width: 80%;
  }

  .icons img {
    max-width: 100%;
  }

  .intro {
    max-width: 80%;
  }

  .sub-main {
    width: 100%;
    font-size: 140%;
  }
}

@media screen and (max-width: 360px) {
  .matthew {
    font-size: 150%;
    margin-top: 15%;
  }

  .intro {
    width: 100%;
  }

  .icons img {
    max-width: 100%;
  }

  .sub-main {
    font-size: 110%;
  }
}



</style>
