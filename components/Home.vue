<template>
  <div class="main">
    <h1 class="main__headline">weTune</h1>
    <h2 class="main__text">the iTunes search tool.</h2>
    <Search />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.main__headline {
  font-size: 7em;
  font-weight: 900;
}
.main__text {
  font-size: 3em;
  color: aqua;
}
</style>
