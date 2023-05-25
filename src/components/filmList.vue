<script>
import filmCard from './filmCard.vue';
import { store } from "../store";
export default {
    data(){
        return {
            store,
        };
    },
    components: {
        filmCard,
    }
};
</script>
<template>
    <div class="film-container">
        <filmCard v-for="film in store.arrFilms" :key="results.poster_path"
        class="film"
        :filmData="film"
        />   
    </div>
</template>
<style lang="scss" scoped>
</style>