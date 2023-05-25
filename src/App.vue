<script>
import inputSearch from './components/inputSearch.vue';
import filmList from './components/filmList.vue';
import axios from "axios";
import { store } from './store';
export default {
  data() {
    return {   
      store,
    };
  },
  components: {
    inputSearch,
    filmList,
  },
  methods: {
        requestDataFromApi() { 
            axios
            .get("https://api.themoviedb.org/3/search/movie", {
              params: {
                api_key: "5f71ca6846ae9e23b392498470b3c9a1",
                query: this.store.searchStr,
              },
            })
            .then(response => (this.store.arrFilms = response.data.results));
        }
    },
    created () {
        this.requestDataFromApi();
    },
};
</script>
<template>
  <inputSearch @performSearch="requestDataFromApi"/>
  <filmList/>
</template>
<style lang="scss">
body {
  margin: 0;
}
</style>

