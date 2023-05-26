<script>
export default {
    props: {
        filmData: Object,
    }
}
</script>
<template>
    <div class="film">
        <div>
            {{ filmdata.images }}
        </div>
        <h2 class="name">
            {{ filmData.name }}
        </h2>
    </div>
</template>
<style lang="scss" scoped>
</style>