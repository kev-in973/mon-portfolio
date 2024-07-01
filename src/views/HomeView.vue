<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logokevB.png">
    <Développeur/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Développeur from '@/components/Développeur.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld, Développeur
  }
}
</script>

<style scoped>
img 
{
  width: 10em
}
</style>
