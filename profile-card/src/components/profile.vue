<template>
    <div class="profile-card">
      <img class="profile-photo" :src="photoUrl" alt="Profile photo" />
      <div class="profile-details">
        <h2>{{ name }}</h2>
        <p>{{ description }}</p>
        <p>{{ intro }}</p>
        <div class="button-group">
            <!-- Profile Link -->
        <a :href="profileUrl" target="_blank" rel="noopener noreferrer">
          <button>Profile</button>
        </a>
        
        <!-- Follow Link -->
        <a :href="followUrl" target="_blank" rel="noopener noreferrer">
            <button>Follow</button>
        </a>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import photo from '@/assets/img/olla2.jpg'
  
  // Data for profile card
  const photoUrl = ref(photo); // Replace with your photo URL
  const name = ref("Ollatomiwa");
  const description = ref("Web Developer & Designer");
  const intro = ref("I build responsive websites with Vue3 and NodeJs");
  
  // Handlers for button actions
    const profileUrl = ref("https://computlife.com.ng"); // Profile link
    const followUrl = ref("https://github.com/Ollatomiwa"); // Follow link
  </script>
  
  <style scoped>
  .profile-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 24px;
  background-color: #0f0f0f;
  border-radius: 40px;
  box-shadow: 0 4px 8px rgba(235, 69, 69, 0.1);
  width: 100%; /* Adjusts width based on screen size */
  max-width: 900px; /* Ensures it doesn’t exceed 900px */
  height: auto; /* Allows height to adjust based on content */
  min-height: 400px; /* Sets a minimum height */
  text-align: center;
  margin: 150px auto 0; /* Centers the card and adds top margin */

}
  .profile-card:hover {
    background-color: rgba(40, 59, 9, 0.356);
  }
  
  .profile-photo {
    width: 100px;
    height: 100px;
    border-radius: 60%;
    object-fit: cover;
  }
  
  .profile-details {
    margin-top: 20px;
  }
  
  h2 {
    margin: 10;
    font-size: 2rem;
    color: #f7f3f3;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  
  p {
    
    margin: 8px 10 16px;
    color: #e2dddd;
    font-size: 1.5rem;
  }
  
  .button-group {
    display: flex;
    gap: 10px;
    justify-content: center;
  }
  
  button {
    padding: 8px 16px;
    font-size: 1.5em;
    border-color: #6af5b4;
    border-radius: 40px;
    cursor: pointer;
    transition: background-color 0.2s;
    
  }
  
  button:first-of-type {
    background-color: #0b0c0cb7;
    color: #fff;
  }
  
  button:last-of-type {
    background-color: #c5bcbb;
    color: #111010;
  }
  
  button:hover {
    background-color: aqua;
    opacity: 0.9;
  }
  
  /* Responsive styling */
  @media (min-width: 600px) {
    .profile-card {
      max-width: 400px;
    }
  
    .profile-photo {
      width: 220px;
      height: 220px;
    }
  }
  </style>
  