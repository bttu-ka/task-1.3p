<template>
    <div class="contact-form">
      <h1 style="background-color: #ff5733; color: white;">Contact Form</h1>
      <form @submit.prevent="submitForm">
        <label for="name">Name:</label>
        <input id="name" v-model="formData.name" required placeholder="Your name" style="margin-bottom: 15px;">
          
        <label for="email">Email:</label>
        <input id="email" v-model="formData.email" type="email" required placeholder="Your e-mail" style="margin-bottom: 15px;">
      
        <label for="message">Message:</label>
        <textarea id="message" v-model="formData.message" rows="8" required placeholder="Any message for me? Type it here." style="margin-bottom: 15px;"></textarea>
      
        <button type="submit" class="submit-button">Submit</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formData: {
          name: '',
          email: '',
          message: ''
        }
      };
    },
    methods: {
      submitForm() {
        console.log('Form Data:', this.formData);
        alert('The form is sent, wait for me to reply to it. Thanks.');
      }
    }
  }
  </script>
  
  <style scoped>
  /* Global Styles */
  body, h1, h2, p, label, input, textarea, button {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
  }
  
  /* Container Styles */
  .contact-form {
    background-color: yellowgreen; /* Updated background color */
    padding: 40px; /* Increased padding to make it taller */
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(237, 173, 24, 0.1);
    max-width: 400px;
    width: 90%;
    color: white; /* Text color */
  }
  
  /* Label Styles */
  label {
    font-weight: bold;
    display: block;
    margin-bottom: 10px; /* Increased margin for more spacing */
    font-family: 'Pacifico', cursive;
    color: #ff5733; /* Label text color */
  }
  
  /* Input and Textarea Styles */
  input[type="text"],
  input[type="email"],
  textarea {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #c9f0d6;
    border-radius: 5px;
    transition: border-color 0.3s;
  }
  
  input[type="text"]:focus,
  input[type="email"]:focus,
  textarea:focus {
    border-color: #72b8a0;
  }
  
  /* Textarea Resize Styles */
  textarea {
    resize: vertical;
  }
  
  /* Submit Button Styles */
  .submit-button {
    background-color: #ff5733; /* Updated button color */
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s;
  }
  
  /* Media Query for Small Screens */
  @media (max-width: 768px) {
    .contact-form {
      width: 100%;
      padding: 20px;
    }
  }
  </style>
  