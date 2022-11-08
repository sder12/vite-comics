<script>
export default {
    name: "MainNav",
    data() {
        return {
            prod: [
                {
                    title: "digital comics",
                    img: "buy-comics-digital-comics.png"
                },
                {
                    title: "dc merchandise",
                    img: "buy-comics-merchandise.png"
                },
                {
                    title: "subscription",
                    img: "buy-comics-subscriptions.png"
                },
                {
                    title: "comic shop locator",
                    img: "buy-comics-shop-locator.png"

                },
                {
                    title: "dc power visa",
                    img: "buy-comics-subscriptions.png"
                }
            ]

        }
    },
    methods: {
        getImage(pathImg) {
            return new URL(pathImg, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <ul class="nav-products">
                <!-- Product -->
                <li class="product" v-for="(item, index) in prod" :key="index">
                    <!-- Img -->
                    <div class="product__image">
                        <img :src="getImage(`../assets/img/${item.img}`)" :alt="item.title">
                    </div>
                    <!-- Text -->
                    <div class="product__text">
                        <span>{{ item.title }}</span>
                    </div>
                </li>
            </ul>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container {
    @include bg-container($primary-color);

    .wrapper {
        @include wrapper(3em, $paddingWrapper);
        color: white;
    }
}

.nav-products {
    @include flex(row, space-around, center);

    .product {
        @include flex(row, center, center);
        gap: 1em;

        &__image {
            width: 40px
        }

        &__text {
            text-transform: uppercase;
            font-size: .8rem;
        }
    }
}
</style>