<template>
    <div class="modal-backdrop" @click.self="close">
      <div class="modal">
        <h2>{{ creation.title }}</h2>
        <p>Date de création: {{ creation.date }}</p>
        <p>Technologies utilisées: {{ creation.technologies.join(', ') }}</p>
        <p>
          <a :href="creation.link" target="_blank">Visiter le site / Voir le fichier</a>
        </p>
        <p v-if="creation.github">
          <a :href="creation.github" target="_blank">Voir sur GitHub</a>
        </p>
        <button @click="close">Fermer</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Modal',
    props: {
      creation: Object
    },
    methods: {
      close() {
        this.$emit('close');
      }
    }
  }
  </script>
  
  <style scoped>
  .modal-backdrop {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  
  .modal {
    background: white;
    padding: 2em;
    border-radius: 8px;
    max-width: 500px;
    width: 100%;
    position: relative;
    z-index: 1001;
  }
  
  button {
    padding: 0.5em;
    background-color: #42b983;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #357a63;
  }
  </style>