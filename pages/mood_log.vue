<!--Track moods page-->
<template>
    <div>
      <h1>Track Your Mood</h1>
      <form @submit.prevent="saveMood"> <!--@submit.prevent -> prevents the page from reloading and displays the selected mood instead-->
        <!--create a drop down-->
        <label for="mood">How are you feeling today?</label>
        <select v-model="mood">
          <option value="happy">Happy</option>
          <option value="sad">Sad</option>
          <option value="neutral">Neutral</option>
        </select>

        <label for="notes"><br>Any notes about how you're feeling?</label>
        <textarea v-model="notes" placeholder="Write your thoughts down..."></textarea>
        <br>
        <button type="submit">Save Mood</button>
      </form>
  
      <!-- <div v-if="submittedMood">
        <h2>Your mood: {{ submittedMood }}</h2>
      </div> -->

      <!-- <div v-if="submittedMood">
        <p>Your mood has been logged!<br> 
          Your Mood: {{ submittedMood }} <br>
          Your note: {{ notes }}</p>
      </div> -->

      <div v-if="moodLog.length>0">
        <h2>Previous Mood Entries:</h2>
        <ul>
          <li v-for="(entry, index) in moodLog" :key="index">
            {{ entry.mood }} : {{ entry.date }} : {{ entry.notes }}
          </li>
        </ul>
      </div>

    
    </div>

  </template>
  
  <script setup>
  import { ref, watch, onMounted } from 'vue';
  
  
  const mood = ref('');
  const submittedMood = ref('');
  const notes = ref(' ');
  const moodLog = ref([]); //array to store the moods notes
  //date
  const currentDate = new Date();
  const year = currentDate.getFullYear();
  const month = String(currentDate.getMonth() + 1).padStart(2, '0');
  const day = String(currentDate.getDate()).padStart(2, '0');
  const formattedDate = month + '.'+ day + '.' + year;

  //save mood entry
  const saveMood = () => {
    submittedMood.value = mood.value;

    //creat new entry to store mood and notes
    const newMoodEntry = {
      mood: mood.value,
      date: formattedDate,
      notes: notes.value,
    };

    //put the new entry into the array
    moodLog.value.push(newMoodEntry);

    //clear the input fields after submission
    mood.value = ' ';
    mood.date = ' ';
    notes.value = ' ';
  };

  //load items from local storage on compenent mount
  onMounted(() => {
    const storedMood = JSON.parse(localStorage.getItem('entry')) || [];
    moodLog.value = storedMood; //populate moodLog with data from localStorage
  });

  
  //watch for changes in moodLog and update local storage
  watch(moodLog, (newValue) => {
    localStorage.setItem('entry', JSON.stringify(moodLog.value));

    console.log('Mood Log was saved to localStorage', newValue);
    console.log('Current localStorage entry:', JSON.parse(localStorage.getItem('entry')));
  }, {deep: true});

  </script>
  
  <style scoped>
  /* styling */
  select {
    margin: 10px;
    padding: 5px;
  }
  
  button {
    padding: 10px 20px;
    background-color: #4caf50;
    color: white;
    border: none;
    cursor: pointer;
  }

  textarea {
    margin: 10px;
  }
  </style>