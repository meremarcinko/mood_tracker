<!--HOME PAGE-->
<template>
    <div>
      <h1>Welcome to Mood Track!</h1>
      <!-- <h2>Keep track of your moods and look back at your history</h2> -->

      <h3>What is a Mood Tracker? How can it be helpful?</h3>
      <p>A mood tracker is a tool used to log your moods as they change day by day.
        When you keep track of your moods, you can observe what could trigger your 
        mood changes. Whether it be situations, the environment or other factors, 
        this is a great way to see how you are impacted.
        <br>
        This can be very helpful if you have particular mental health conditions like 
        depression or anxiety where you can label and regulate your moods as they come.
        <br>
        Mood tracking can also be beneficial if you dont have mental health conditions, 
        it can help you have a better understanding of yourself, your emotions and how 
        to improve your mood.
      </p>
      <div class="container">
        <div class="center">
          <nuxt-link to="/mood_log" class="button">Go to Mood Log</nuxt-link>
        </div>
      </div>
    </div>
  </template>
  <script setup>
  // You can add any setup code for this page here
  </script>
  
  <style scoped>
  h1 {
    color: #7c12e6 ;
    text-align: center;
    font-family: Garamond, serif;
    font-style: italic;
    font-variant: small-caps;
    margin-top: 75px;
    font-size: 50px;
    font-weight: bold;
  }

  h2{
    text-align: center;
    margin-right: 200px;
    margin-left: 200px;
    max-width: 800px;
    margin-bottom: 50px;
  }

  h3{
    text-align: center;
    margin-right: 200px;
    margin-left: 200px;
    max-width: 800px;
  }

  p {
    text-align: center;
    font-size: 20px;
    margin-left: 150px;
    margin-right: 150px;
    max-width: 800px;
  }
  /* .button {
    background-color: #2222e0;
    border: none;
    border-radius: 12px;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
  } */

  .button {
    background: linear-gradient(90deg, #b005e9, #6d01b0);
    color: white;
    font-weight: 600;
    font-size: 1rem;
    padding: 0.8rem 2rem;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    text-transform: uppercase;
    letter-spacing: 1px;
    box-shadow: 0 4px 20px rgba(255, 58, 130, 0.3);
    text-align: center;
  }
  
  .container {
    padding: 200 px;
    position: relative;
    border: 3px rgb(124, 25, 216);
  }

  .center {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 200px;
    border: 3px rgb(124, 25, 216);
  }

  .button:hover{
    transform: translateY(-2px);
    box-shadow: 0 6px 25px rgba(255, 58, 130, 0.4);
  }

  .gradient-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
    overflow: hidden;
  }
  </style>