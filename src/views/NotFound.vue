<!-- src/views/NotFound.vue -->
<template>
    <div class="not-found">
      <img src="@/assets/logokevB.png" alt="404 Image" />
      <h1>404</h1>
      <p>La page que vous recherchez n'existe pas.</p>
      <router-link to="/">Retour à la page d'accueil</router-link>
    </div>
  </template>
  
  <script>
  export default {
    name: 'NotFound'
  }
  </script>
  
  <style scoped>
  .not-found {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    text-align: center;
  }
  
  .not-found img {
    max-width: 300px;
    margin-bottom: 1em;
  }
  
  .not-found h1 {
    font-size: 6em;
    margin: 0.5em 0;
  }
  
  .not-found p {
    font-size: 1.5em;
    margin-bottom: 1em;
  }
  
  .not-found a {
    color: #42b983;
    text-decoration: none;
    font-weight: bold;
  }
  
  .not-found a:hover {
    text-decoration: underline;
  }
  </style>