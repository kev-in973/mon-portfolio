<template>
  <header>
    <div class="logo">
      <router-link to="/">
        <img src="../assets/logokevB.png" alt="Logo" />
      </router-link>
    </div>
    <nav>
      <ul>
        <li><a href="home">Home</a></li>
        <li><a href="about">About</a></li>
        <li><a href="contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em;
  background-color: #333;
  color: #fff;
}

.logo img {
  height: 50px;
}

nav ul {
  list-style-type: none;
  display: flex;
  gap: 1em;
}

nav a {
  color: #fff;
  text-decoration: none;
}

nav a:hover {
  text-decoration: underline;
}
</style>