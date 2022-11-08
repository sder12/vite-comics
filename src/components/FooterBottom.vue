<script>
export default {
    name: "FooterBottom",
    data() {
        return {
            socials: [
                {
                    name: "facebook",
                    img: "footer-facebook.png",
                    link: "#"
                },
                {
                    name: "twitter",
                    img: "footer-twitter.png",
                    link: "#"
                },
                {
                    name: "youtube",
                    img: "footer-youtube.png",
                    link: "#"
                },
                {
                    name: "pinterest",
                    img: "footer-pinterest.png",
                    link: "#"
                },
                {
                    name: "periscope",
                    img: "footer-periscope.png",
                    link: "#"
                },
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
            <footer class="footer footer-bottom">
                <section class="footer__signup">
                    <div>
                        <a href="#">sign-up now!</a>
                    </div>
                </section>
                <section class="footer__social">
                    <ul>
                        <li>
                            <span>follow-us</span>
                        </li>
                        <li v-for="(social, index) in socials" :key="index">
                            <a :href="social.link">
                                <img :src="getImage(`../assets/img/${social.img}`)" :alt="social.name">
                            </a>
                        </li>
                    </ul>
                </section>
            </footer>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container {
    @include bg-container($footer-color);
    min-height: $footer-bottom-height;

    .wrapper {
        @include wrapper(3em, $paddingWrapper);
    }
}

.footer {
    @include flex(row, space-between, center);
    text-transform: uppercase;

    &__signup {
        border: 1px solid $primary-color;
        padding: 1em 1em;

        a {
            color: white;

        }
    }

    &__social ul {
        @include flex(row, flex-end, center);
        gap: 1em;

        span {
            color: $primary-color;
        }
    }
}
</style>