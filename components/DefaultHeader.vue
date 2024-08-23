<template>
  <header class="portal-header">
    <div class="container">
      <nav>
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/dashboard">Dashboard</a></li>
          <li><a href="/profile">Profile</a></li>
          <li><a href="/settings">Settings</a></li>
        </ul>
      </nav>
      <div class="user-actions">
        <button class="notifications">Notifications</button>
        <button class="logout">Logout</button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "DefaultHeader",
};
</script>

<style scoped>
.portal-header {
  background-color: #f8f9fa;
  padding: 1rem 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

nav ul {
  list-style-type: none;
  display: flex;
  gap: 1rem;
}

nav a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
}

.user-actions {
  display: flex;
  gap: 1rem;
}

button {
  padding: 0.5rem 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.notifications {
  background-color: #007bff;
  color: white;
}

.logout {
  background-color: #dc3545;
  color: white;
}
</style>
