<template>
  <div class="about">
    <img alt="Vue logo" src="../assets/logokevB.png">
    <h1>Mon parcours</h1>
    <Développeur/>

    <header>
      <a href="images/foto cv.jpg" target="_blank">
        <img alt="Vue logo" src="../assets/kev3d.png">
      </a>
      <h1>Developpeur Web Junior</h1>
      <h2>Ladouceur Kevin</h2>
    </header>
    <nav>
      <ul>
        <li>
          <address>
            <a href="https://www.google.fr/maps/place/590+Av.+Charles+de+Gaulle,+74800+La+Roche-sur-Foron/@46.0720775,6.304771,17z/data=!3m1!4b1!4m6!3m5!1s0x478c751ddb3bf74f:0x533266dc7d42ed6f!8m2!3d46.0720738!4d6.3073459!16s%2Fg%2F11cpb84y0h?entry=ttu">
              590 avenue Jean Jaures <br> 74800 La Roche-sur-Foron
            </a>
            <a href="mailto:kevin-ladouceur.97351@gmail.com">kevin-ladouceur.97351@gmail.com</a>
            <a href="tel:0607080910">0607080910</a>
          </address>
        </li>
      </ul>
    </nav>
    <main>
      <section class="about">
        <h3 class="about__title">A propos</h3>
        <p class="about__description">Lorem ipsum dolor sit amet, consectetur adipisicing <br>elit.Debitis maxime, illum rerum aut necessitatibus dicta <br>fuga nobis! <br>Quasi, rerum, impedit, assumenda nesciunt amet <br>molestiae error dolor maxime cum officia placeat.</p>
      </section>
      <section class="languages">
        <h3 class="languages__title">Langues parlées</h3>
        <ul class="languages__list">
          <li class="languages__item">Français - Langue maternelle</li>
          <li class="languages__item">Anglais - Intermédiaire</li>
          <li class="languages__item">Espagnol - Débutant</li>
        </ul>
      </section>
      <section class="interests">
        <h3 class="interests__title">Centres d'intérêt</h3>
        <ul class="interests__list">
          <li class="interests__item">Chant</li>
          <li class="interests__item">Fitness</li>
          <li class="interests__item">Randonnée</li>
          <li class="interests__item">Voyages</li>
        </ul>
      </section>
      <section class="experiences">
        <h3 class="experiences__title">Expériences professionnelles</h3>
        <span>Intitulé du poste chez Nom de l'entreprise</span> <br>
        <p>Du XXX au XXX</p>
        <ul class="experiences__list">
          <li class="experiences__item">Mission1</li>
          <li class="experiences__item">Mission2</li>
          <li class="experiences__item">Mission3</li>
        </ul>
        <br>
        <span>Intitulé du poste chez Nom de l'entreprise</span> <br>
        <p>Du XXX au XXX</p>
        <ul class="experiences__list">
          <li class="experiences__item">Mission1</li>
          <li class="experiences__item">Mission2</li>
          <li class="experiences__item">Mission3</li>
          <li class="experiences__item">Mission4</li>
        </ul>
        <br>
        <span>Intitulé du poste chez Nom de l'entreprise</span> <br>
        <p>Du XXX au XXX</p>
        <ul class="experiences__list">
          <li class="experiences__item">Mission1</li>
          <li class="experiences__item">Mission2</li>
        </ul>
        <br>
      </section>
      <section class="diplomes">
        <h3 class="diplomes__title">Diplomes/Formations</h3>
        <span>Diplomes/Formations n°1</span> <br>
        <p>Du XXX au XXX</p>
        <p>Nom de l'école</p> <br>
        <span>Diplomes/Formations n°2</span> <br>
        <p>Du XXX au XXX</p>
        <p>Nom de l'école</p> <br>
      </section>
      <section class="competences">
        <h3 class="competences__title">Compétences</h3>
        <ul class="competences__list">
          <li class="competences__item">HTML 5 - Expert</li>
          <li class="competences__item">CSS 3 - Intermédiaire</li>
          <li class="competences__item">Github - Débutant</li>
          <li class="competences__item">....</li>
        </ul>
      </section>
    </main>
    <footer>
      
    </footer>
  </div>
</template>

<script>
import Développeur from '@/components/Développeur.vue'

export default {
  name: 'AboutView',
  components: {
    Développeur
  }
}
</script>

<style scoped>
img {
  width: 10em;
}
</style>