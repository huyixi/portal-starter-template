<template>
  <div class="home">
    <main class="container">
      <h1>Welcome to Our Portal</h1>
      <p>This is the main page of our application. Here you can find the latest updates and navigate to different sections.</p>
    </main>
  </div>
</template>

<script>
export default {
  name: "HomePage",
};
</script>

<style scoped>
.home {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.container {
  flex: 1;
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

p {
  font-size: 1.1rem;
  line-height: 1.6;
}
</style>
