<template>
  <div class="profile">
    <DefaultHeader />
    <main class="container">
      <h1>User Profile</h1>
      <div class="profile-info">
        <div class="avatar">
          <img src="~/assets/img/avatar-ph.jpeg" alt="User Avatar" />
        </div>
        <div class="user-details">
          <h2>{{ user.name }}</h2>
          <p>Email: {{ user.email }}</p>
          <p>Member since: {{ user.joinDate }}</p>
        </div>
      </div>
      <div class="profile-actions">
        <button @click="editProfile" class="edit-profile">Edit Profile</button>
        <button @click="changePassword" class="change-password">Change Password</button>
      </div>
    </main>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

definePageMeta({
  middleware: "auth",
});

interface User {
  name: string;
  email: string;
  joinDate: string;
}

const user = ref<User>({
  name: "John Doe",
  email: "john.doe@example.com",
  joinDate: "January 1, 2023",
});

const editProfile = () => {
  // Implement edit profile functionality
  console.log("Edit profile clicked");
};

const changePassword = () => {
  // Implement change password functionality
  console.log("Change password clicked");
};
</script>

<style scoped>
.profile {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.container {
  flex: 1;
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

.profile-info {
  display: flex;
  align-items: center;
  margin-bottom: 2rem;
}

.avatar img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 2rem;
}

.user-details h2 {
  font-size: 1.8rem;
  margin-bottom: 0.5rem;
}

.user-details p {
  font-size: 1.1rem;
  margin-bottom: 0.5rem;
}

.profile-actions {
  display: flex;
  gap: 1rem;
}

button {
  padding: 0.5rem 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 1rem;
}

.edit-profile {
  background-color: #007bff;
  color: white;
}

.change-password {
  background-color: #6c757d;
  color: white;
}
</style>
