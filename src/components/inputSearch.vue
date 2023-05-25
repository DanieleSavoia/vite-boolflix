<script>
export default {
    data(){
        return {
            
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
            <input type="text" placeholder="Search Film/Series">
            <button>Search</button>
            <button>Reset</button> 
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