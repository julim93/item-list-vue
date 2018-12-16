<template>
  <div>
    <div class="navbar">
      <img class="logo" alt="Vue logo" src="../assets/logo.png">
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Layout',
}
</script>

<style scoped>
.navbar {
  background-color: #625876;
  color: white;
  height: 60px;
}
.logo {
  height: 40px;
  margin-top: 8px;
}
</style>
