<template>
  <div>
    <section id="presentation">
      <h1>Présentation</h1>
      <p>Bonjour, je m'appelle Kevin Ladouceur .</p>
      <p>Je suis un jeune rookie développeur web passionné par le digital, la création de site, et tous ce qui touche le monde du numérique.</p>
    </section>
    <section id="creations">
      <h1>Créations</h1>
      <div class="creations-grid">
        <div v-for="creation in creations" :key="creation.id" class="creation-item" @click="openModal(creation)">
          <img :src="creation.image" :alt="creation.title">
          <h3>{{ creation.title }}</h3>
        </div>
      </div>
      <Modal v-if="selectedCreation" :creation="selectedCreation" @close="selectedCreation = null"/>
    </section>
    <section id="contact">
      <h1>Contact</h1>
      <form @submit.prevent="submitForm">
        <label for="name">Nom/Prénom:</label>
        <input type="text" id="name" v-model="form.name" required>

        <label for="subject">Objet:</label>
        <input type="text" id="subject" v-model="form.subject" required>

        <label for="message">Message:</label>
        <textarea id="message" v-model="form.message" required></textarea>

        <button type="submit">Envoyer</button>
      </form>
    </section>
  </div>
</template>

<script>
import Modal from '@/components/Modal.vue'

export default {
  name: 'HomeView',
  components: {
    Modal
  },
  data() {
    return {
      creations: [
        { 
          id: 1, 
          title: 'Création 1', 
          image: require('@/assets/numero-1.png'), 
          date: '01/01/2021', 
          technologies: ['HTML', 'CSS', 'JavaScript'], 
          link: 'https://www.example.com', 
          github: 'https://github.com/user/repo1',
          details: 'Détails de la création 1...' 
        },
        { 
          id: 2, 
          title: 'Création 2', 
          image: require('@/assets/numero-2.png'), 
          date: '01/06/2021', 
          technologies: ['Vue', 'Node.js'], 
          link: 'https://www.example2.com', 
          github: null,
          details: 'Détails de la création 2...' 
        },
         
        { 
          id: 3, 
          title: 'Création 3', 
          image: require('@/assets/numero-3.png'), 
          date: '01/06/2021', 
          technologies: ['Vue', 'Node.js'], 
          link: 'https://www.example2.com', 
          github: null,
          details: 'Détails de la création 3...' 
        },
        

        // Ajoute d'autant de créations que nécessaire
      ],
      selectedCreation: null,
      form: {
        name: '',
        subject: '',
        message: ''
      }
    }
  },
  methods: {
    openModal(creation) {
      this.selectedCreation = creation;
    },
    submitForm() {
      const email = process.env.VUE_APP_CONTACT_EMAIL;
      const mailtoLink = `mailto:${email}?subject=${encodeURIComponent(this.form.subject)}&body=${encodeURIComponent(this.form.message)}%0D%0A%0D%0ANom: ${encodeURIComponent(this.form.name)}`;
      window.location.href = mailtoLink;
    }
  }
}
</script>

<style scoped>
section {
  padding: 2em 0;
}

.creations-grid {
  display: flex;
  gap: 9em;
}

.creation-item {
  cursor: pointer;
}

form {
  display: flex;
  flex-direction: column;
  gap: 1em;
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