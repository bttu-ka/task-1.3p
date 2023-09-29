<template>
  <div class="about-container">
    <header class="custom-header">
      <h1 class="custom-title">Akshat's Portfolio</h1>
    </header>
    <div class="content-container">
      <div class="intro-container">
        <h2 class="custom-subtitle">{{ name }}</h2>
        <p class="custom-intro">{{ intro }}</p>
      </div>
      
      <div v-for="project in projects" :key="project.title" class="project-container">
        <h2 class="project-title">{{ project.title }}</h2>
        <p class="project-description">{{ project.description }}</p>
        <a :href="project.link" target="_blank" rel="noopener noreferrer" class="custom-link">View</a>
      </div>
      <div class="contact-container">
        <p class="contact-title">My credentials:</p>
        <p class="contact-info">Email: {{ email }}</p>
        <p class="contact-info">Student ID: {{ studentid }}</p>
        <p class="contact-info">Phone: {{ phone }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      intro: 'This is my portfolio webste showcasing my projects and my credentials.',
      studentid: 'S223307311',
      
      projects: [
        {
          title: 'Project-1',
          description: 'For this project, I have created a To-Do list app using HTML, CSS and a variety of Vue3 concepts. ',
          link: 'https://github.com/bttu-ka/2.1C'
        },
        {
          title: 'Project-2',
          description: 'For this project, I have created a website called Travelscape,which users can use to plan adn organize their trips efficiently.',
          link: 'https://github.com/bttu-ka/task2.2c'
        },
        {
          title: 'Project-3',
          description: 'For this project, I have created a Responsive webpage using HTML and CSS.',
          link: 'https://github.com/bttu-ka/TASK1.2P-RESPONSIVE-WEB-APPS-'
        },
      ],
      email: 'akshataswa@deakin.us',
      phone: '0424XXXXXX'
    };
  }
};
</script>

<style scoped>

body {
  background-color: white;
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.about-container {
  width: 100%;
  max-width: 1200px;
  padding: 20px;
  box-sizing: border-box;
}


.custom-header {
  background-color: #3498db;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}

.custom-title {
  font-family: 'arial',sans-serif;
  margin: 0;
  font-size: 36px;
}


.content-container {
  background-color: #fff;
  border-radius: 10px;
  padding: 30px;
  margin: 20px 0;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
}

.intro-container {
  text-align: center;
}

.custom-subtitle {
  font-family: 'arial',sans-serif;
  color: #3498db;
  font-size: 24px;
}

.custom-intro {
  color: #555;
  font-size: 18px;
  margin-top: 20px;
}


.skills-container {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.skill {
  background-color: pink;
  color: #fff;
  padding: 8px 16px;
  margin: 5px;
  border-radius: 3px;
  text-transform: uppercase;
  font-weight: bold;
}


.project-container {
  background-color: #ecf0f1;
  border-radius: 5px;
  padding: 20px;
  margin: 20px 0;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  text-align: center;
}

.project-title {
  color: #3498db;
  font-family: 'ariel', sans-serif;
  font-size: 24px;
  font-weight: bold;
}

.project-description {
  color: #333;
  margin-top: 10px;
}

.custom-link {
  display: inline-block;
  background-color: #27ae60;
  color: #fff;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  transition-duration: 0.4s;
  font-weight: bold;
  margin-top: 10px;
}

.custom-link:hover {
  background-color: #1e8449;
}


.contact-container {
  background-color: #ecf0f1;
  border-radius: 5px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  text-align: center;
  font-weight: bold;
}


.contact-title {
  color: #3498db;
  font-size: 24px;
  font-weight: bold;
}

.contact-info {
  color: #333;
  margin-top: 10px;
  font-weight: bold;
}

.contact-info:hover {
  color: #000;
}
</style>
