<script>
export default {
    name: "MainNav",
    data() {
        return {
            prod: [
                {
                    title: "digital comics",
                    img: "buy-comics-digital-comics.png",
                    imgSize: "bigger"
                },
                {
                    title: "dc merchandise",
                    img: "buy-comics-merchandise.png",
                    imgSize: ""
                },
                {
                    title: "subscription",
                    img: "buy-comics-subscriptions.png",
                    imgSize: ""
                },
                {
                    title: "comic shop locator",
                    img: "buy-comics-shop-locator.png",
                    imgSize: "bigger",
                },
                {
                    title: "dc power visa",
                    img: "buy-dc-power-visa.svg",
                    imgSize: ""
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
            <!-- Nav Products -->
            <ul class="nav-products">
                <!-- Product -->
                <li class="product" v-for="(item, index) in prod" :key="index">
                    <!-- Img -->
                    <div class="product__image" :class="item.imgSize == 'bigger' ? '' : 'space-gap'">
                        <img :src="getImage(`../assets/img/${item.img}`)" :alt="item.title"
                            :class="item.imgSize == 'bigger' ? 'scale-down' : ''">
                    </div>
                    <!-- Text -->
                    <div class="product__text">
                        <span>{{ item.title }}</span>
                    </div>
                </li>
            </ul>
            <!-- / Nav Products -->
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

//Layout
.container {
    @include bg-container($primary-color);

    .wrapper {
        @include wrapper(1em, $paddingWrapper);
        color: white;
    }
}

//Content
.nav-products {
    @include flex(row, space-around, center);



    //IMG + TXT
    .product {
        @include flex(row, center, center);
        cursor: pointer;
        padding: 1em 1em;

        &:hover {
            background-color: lighten($primary-color, 10%);
        }


        // IMAGE
        &__image {
            width: 45px;

            .scale-down {
                width: 33px;
            }
        }

        .space-gap {
            margin-right: .6em;
        }

        // TEXT
        &__text {
            text-transform: uppercase;
            font-size: .8rem;
        }


    }
}
</style>