<template>
  <div class="dashboard">
    <h1 class="welcome">Welcome</h1>
    <div class="links">
      <a href="#">Link 1</a>
      <a href="#">Link 2</a>
      <a href="#">Link 3</a>
      <a href="#">Link 4</a>
    </div>
    <form @submit.prevent>
      <input class="input-playlist" type="text" placeholder="Search" />
    </form>
    <div class="scroll-section">
    </div>
  </div>
</template>

<script>
import '../assets/styles/dashboard.css';
export default {
  name: 'Dashboard',
}
</script>


