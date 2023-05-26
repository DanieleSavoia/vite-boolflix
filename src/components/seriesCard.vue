<script>
export default {
    props: {
        seriesData: Object,
    }
}
</script>
<template>
    <div class="flip-card">
    <div class="flip-card-inner">
    <div class="flip-card-front">
        <img :src="`https://image.tmdb.org/t/p/w342${seriesData.poster_path}`" :alt="seriesData.title" style="width:300px;height:400px;">
    </div>
    <div class="flip-card-back">
        <div>
           titolo: <b>{{ seriesData.title }}</b>
        </div> 
        <div >
           titolo originale: <b>{{ seriesData.original_title }}</b>
        </div>
        <div >
           voto: <b>{{ seriesData.vote_average }}</b>
        </div>
        <div >
           trama: <b>{{ seriesData.overview }}</b>
        </div>
    </div>
  </div>
</div>
</template>
<style lang="scss" scoped>
body {
  font-family: Arial, Helvetica, sans-serif;
}

.flip-card {
  background-color: transparent;
  width: 300px;
  height: 400px;
  perspective: 1000px;
  border: 1px solid white;
  margin-top: 10px;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  transition: transform 0.6s;
  transform-style: preserve-3d;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.flip-card-front {
  background-color: #bbb;
  color: black;
}

.flip-card-back {
  background-color: #000000;
  color: white;
  transform: rotateY(180deg);
}
</style>