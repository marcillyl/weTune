<template>
  <div class="search">
    <h3 class="search__headline">Type an artist name</h3>
    <form @submit.prevent="submit">
      <input type="text" v-model="search" class="search__input" />
    </form>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      search: "",
    };
  },
  methods: {
    submit() {
      this.$router.push(`results/${this.search}`);
    },
  },
};
</script>

<style>
.search {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.search__headline {
  font-size: 1.1em;
  margin: 10pt;
}
.search__input {
  padding: 4pt;
  background-color: #ffffff22;
  border: solid thin #ffffff33;
}
</style>
