<template>
  <div class="home">
    <h1>Utah Snow</h1>
    <h3>Your Hub for Utah Ski/Snowboard Resort Information</h3>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 5em 0;
  height: 30em;
  border-radius: 1em;
  background: linear-gradient(rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.45)),
    url("../../public/images/snowbird.jpg");
  color: white;
  padding: 1em 2em;
  margin: 3em 0;
  font-family: "Times New Roman", Times, serif;
}

h1 {
  font-size: 60px;
  margin: 0;
}
</style>
