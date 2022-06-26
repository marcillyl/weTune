<template>
  <article class="artist">
    <h4 class="artist__headline">{{ artistName }}</h4>
    <p class="artist__text">{{ albumName }}</p>
  </article>
</template>

<script>
export default {
  props: ["albumName", "image", "artistName", "url"],
};
</script>

<style>
.artist {
  max-width: 300pt;
  margin: 17pt;
  background-color: crimson;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 10pt;
}
</style>
