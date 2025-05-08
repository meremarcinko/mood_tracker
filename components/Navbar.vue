<!-- components/Navbar.vue -->
<template>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400..900&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400..900&family=Old+Standard+TT:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">  
  </head>
  <nav class="navbar">
    <!-- <h2>This is the Navbar</h2> -->

    <!-- Navigation links can be added here -->
    
    <ul>
      <li><NuxtLink to="/" class="nav-tab">Home</NuxtLink></li>
      <li><NuxtLink to="/mood_log" class="nav-tab">Log</NuxtLink></li>
      <li><NuxtLink to="/mood_history" class="nav-tab">History</NuxtLink></li>
      <li><NuxtLink to="/articles" class="nav-tab">Articles</NuxtLink></li>
    </ul>
   
  </nav>
</template>

<script setup>
// no script needed right now
</script>

<style scoped>
.navbar {
  display: flex;
  background-color: lightblue;
  padding: 0;
  margin: 0;
  height: 60px;
  /* text-align: center;
  color: #0000ff; */
}

.nav-tab {
  display: flex;
  align-items: center;
  height: 100%;
  width: 100%;
  justify-content: center;
  text-decoration: none;
  transition: 0.3s;
}

.nav-tab:hover {
  background-color: blueviolet;
}

ul {
  display: flex;
  flex:1;
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
}

li {
  display: flex;
  flex: 1;
  height: 100%;
  align-items: center;
  justify-content: center;
  border: 1px solid red;
  font-family: "cinzel", serif;
  font-optical-sizing: auto;
  font-weight: 700;
  font-style: normal;
}

.router-link-active {

}
.router-link-active {

}

.router-link-exact-active {
  background-color: blueviolet;
}
</style>