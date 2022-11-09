<script>
export default {
    name: "MainCard",
    props: {
        cardThumb: String,
        cardPrice: String,
        cardSeries: String,
        cardType: String,
    },
    methods: {
        cardType() {
            if (this.cardType === "graphic novel") {
                return "graphic"
            } else if (this.cardType === "comic book") {
                return "comics"
            } else {
                return "else-type"
            }
        }
    }
}
</script>

<template>
    <div class="card-wrapper">
        <div class="card-img" :class="cardType()">
            <img :src="cardThumb" :alt="cardSeries">
            <span class="card-price"> {{ cardPrice }}</span>
        </div>
        <div class="card-series">
            <h4>{{ cardSeries }}</h4>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.card-wrapper {
    width: calc(100% / 6);
    @include flex(column, flex-start, center);
    margin-top: 2em;
    cursor: pointer;

    &:hover .card-img {
        opacity: .5;
    }
}

.card-img {
    width: 10em;
    height: 10em;
    position: relative;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }


    &.graphic {
        border-bottom: 3px solid fuchsia;
    }

    &.comics {
        border-bottom: 3px solid $primary-color;
    }

    &.else-type {
        border-bottom: 3px solid white;
    }

    .card-price {
        font-size: .8rem;
        background-color: black;
        color: white;
        padding: .3em .3em;
        position: absolute;
        bottom: 0;
        right: 0;
    }
}

.card-series {
    align-self: flex-start;
    text-transform: uppercase;
    font-size: .9rem;
    padding: 1em 1em;
}
</style>