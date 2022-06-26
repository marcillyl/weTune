<template>
  <div>
    <Header />
    <div class="container">
      <h1 class="container__headline">
        Results for
        <span class="container__headline--name">{{ $route.params.id }}</span>
      </h1>
      <div v-if="albumExists" class="albums">
        <div v-for="album in albumData" v-bind:key="album.id">
          <Card
            :artistName="album.artistName"
            :albumName="album.collectionCensoredName"
          />
        </div>
      </div>
      <div v-else>Could not find album</div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Card from "../../components/Card.vue";
export default {
  asyncData({ params }) {
    return axios
      .get(`https://itunes.apple.com/search?term=${params.id}&entity=album`)
      .then((response) => {
        return { albumData: response.data.results };
      });
  },
  components: {
    Card,
  },
  middleware: "search",
  methods: {
    picker(index) {
      return index % 2 == 0 ? "red" : "blue";
    },
  },
  computed: {
    albumExists() {
      return this.albumData.length > 0;
    },
  },
};
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.container__headline {
  font-size: 1.7em;
  margin: 10pt 0;
}
.container__headline--name {
  color: aqua;
}
</style>
