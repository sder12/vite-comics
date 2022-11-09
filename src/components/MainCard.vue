<script>
export default {
    name: "MainCard",
    props: {
        cardThumb: String,
        cardPrice: String,
        cardSeries: String,
        cardType: String,
    }
}
</script>

<template>
    <div class="card-wrapper">
        <div class="card-img">
            <img :src="cardThumb" :alt="cardSeries">
        </div>
        <div class="card-series">
            {{ cardType }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.card-wrapper {
    width: calc(100% / 6);
    @include flex(column, center, center);
    margin-top: 1.5em;
}

.card-img {
    width: 150px;
    height: 150px;


    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}
</style>