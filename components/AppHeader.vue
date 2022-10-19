<template>
  <section class="masthead" role="img" aria-label="Image Description">
    <h1>Nuxt Food App</h1>
    <button>Find a restaurant</button>
  </section>
</template>

<script>
export default {};
</script>

<style lang="css" scoped>
.masthead {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 100%;
  height: 80vh;
  padding: 40px;
  margin-bottom: 60px;
  overflow: hidden;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;

  background-image: url("../assets/headerimg.jpg");
}
h1 {
  font-style: normal;
  font-weight: bold;
  color: #eee;
  font-size: 8vmin;
  letter-spacing: 0.03em;
  line-height: 1;
  text-shadow: 1px 2px 4px rgba(0, 0, 0, 0.8);
  margin-bottom: 30px;
}
</style>
