<script>
import { ref, onMounted, onUnmounted } from 'vue';
import AppMain from "@/components/AppMain.vue";
import ProjectsMain from "@/components/ProjectsMain.vue";
import AboutMeMain from "@/components/AboutMeMain.vue";
import ContactMain from "@/components/ContactMain.vue";

export default {
  components: {
    AppMain,
    ProjectsMain,
    AboutMeMain,
    ContactMain
  },
  setup() {
    const intro = ref('Home 🏠');
    const project = ref('Projects💻');
    const about = ref('About Me 📖');
    const contact = ref('Contact Me 📧');

    const check = () => {
      const screenWidth = window.innerWidth;

      if (screenWidth < 1000) {
        intro.value = '🏠';
        project.value = '💻';
        about.value = '📖';
        contact.value = '📧';
      } else {
        intro.value = 'Home 🏠';
        project.value = 'Projects 💻';
        about.value = 'About me 📖';
        contact.value = 'Contact me📧';
      }
    };

    const smoothScrollTo = (targetId) => {
      const targetElement = document.getElementById(targetId);

      if (targetElement) {
        const offset = 80; // Adjust this offset based on your design
        const targetPosition = targetElement.offsetTop - offset;

        window.scrollTo({
          top: targetPosition,
          behavior: 'smooth',
        });
      }
    };

    // Call the check method on component mount
    onMounted(() => {
      check();
      document.title = "Matthew's Portfolio";
    });

    // Listen for window resize events and update intro accordingly
    onUnmounted(() => {
      window.removeEventListener('resize', check);
    });

    // Listen for window resize events and update intro accordingly
    window.addEventListener('resize', check);

    // Return reactive variables and methods
    return {
      intro,
      project,
      about,
      contact,
      smoothScrollTo,
    };
  },
};
</script>


<template>
  <div class="navbar">
    <a @click="smoothScrollTo('intro')"> {{ intro }} </a>
    <a @click="smoothScrollTo('projects')"> {{ project }} </a>
    <a @click="smoothScrollTo('about')"> {{ about }}</a>
    <a @click="smoothScrollTo('contact')"> {{ contact }} </a>
  </div>

  <AppMain> </AppMain>
  <ProjectsMain> </ProjectsMain>
  <AboutMeMain> </AboutMeMain>
  <ContactMain> </ContactMain>
  
</template>

<style>
body {
  font-family: 'IBM Plex Sans', sans-serif;
  margin: 0;
  padding: 0;
  background-image: linear-gradient(#181818, #131313);
  overflow: overlay;
  user-select: none;
}


.navbar {
  min-width: 200px;
  width: 50%;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  text-align: center;
  margin: 0 auto;
  margin-top: 1%;
  background-color: #333;
  overflow: hidden;
  position: sticky;
  top: 0;
  z-index: 1000;
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.navbar a {
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  cursor: pointer;
}

.navbar a:hover {
  background-color: #ddd;
  color: black;
}



::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}

::-webkit-scrollbar-thumb {
  background: azure ;
}

::-webkit-scrollbar-track {
  background:linear-gradient(#181818, #131313);
}

</style>


