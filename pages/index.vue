<!--HOME PAGE-->
<template>
    <div>
      <h1>Welcome to Mood Track!</h1>
      <p>Keep track of your moods and look back at your history</p>

      <h2>What is a Mood Tracker? How can it be helpful?</h2>
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
      <nuxt-link to="/mood_log" class="button">Go to Mood Log</nuxt-link>
    </div>
  </template>
  <script setup>
  // You can add any setup code for this page here
  </script>
  
  <style scoped>
  h1 {
    color: #2222e0;
    text-align: center;

  }
  .button {
    background-color: #2222e0;
    border: none;
    border-radius: 12px;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
  }

  .button:hover{
    background-color: #2222e0;
    color: rgb(42, 225, 106);
  }
  </style>