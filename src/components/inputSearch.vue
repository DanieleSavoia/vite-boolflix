<script>
import { store } from '../store';
export default {
    data(){
        return {
            store,
        
        };
    }
}
</script>
<template>
    <div class="appSearch">
        <h1 class="title">
            Boolflix
        </h1>
        <div>
            <input type="text" placeholder="Search Film/Series" v-model="store.searchStr">
            <button @click="$emit('performSearch')">Search</button>
            <button @click="$emit('clearSearch')">Reset</button>
        </div>  
    </div>
    
    
</template>
<style lang="scss" scoped>
.title {
 color: red;
}

.appSearch {
    display:flex;
    justify-content: space-between;
    align-items: center;
    background-color: black;
}
</style>