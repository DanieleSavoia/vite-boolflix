<script>
import seriesCard from './seriesCard.vue'
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
        seriesCard,
    }
};
</script>
<template>
    <div class="title">Film</div>
    <div class="container">
        <filmCard v-for="film in store.arrFilms" :key="film.id" 
        class="film"
        :filmData="film"
        />   
    </div>
    <div class="title">Series</div>
    <div class="container">
        <seriesCard v-for="series in store.arrSeries" :key="series.id" 
        class="series"
        :seriesData="series"
        />   
    </div>
</template>
<style lang="scss" scoped>

.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    background-color: rgb(119, 118, 118);
   
}
.title {
    font-size: 30px;
    background-color: rgb(163, 55, 55);
}
</style>