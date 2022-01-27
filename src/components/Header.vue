<template>
  <div class="header">
    <h1>MatheLock</h1>
    <a href="https://github.com/juanrtalmeida" target="_blank">
      <img src="../../public/GitHub-Mark-Light-32px.png" alt=""
    /></a>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  color: rgb(130, 212, 185);
  font-family: "Poppins";
  font-weight: bold;
}
</style>
