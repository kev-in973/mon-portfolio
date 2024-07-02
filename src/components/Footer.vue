<template>
    <footer>
      <div>
        <a href="https://www.github.com" target="_blank">
          <img alt="github" src="../assets/github.png">
        </a>
      </div>
      <div>
        Dernière mise à jour : {{ lastUpdated }}
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
    data() {
      return {
        lastUpdated: new Date().toLocaleDateString()
      };
    }
  };
  </script>
  
  <style scoped>
  footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1em;
    background-color: #333;
    color: #fff;
  }
  img {
    width: 2em;
    margin: 0 0.5em;
  }
  </style>