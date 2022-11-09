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
            <!-- Footer Bottom -->
            <footer class="footer">
                <!-- Left - sign up -->
                <section class="footer__signup">
                    <div>
                        <a href="#">sign-up now!</a>
                    </div>
                </section>
                <!-- Right - follow us -->
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
            <!-- / Footer Bottom -->
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// Layout
.container {
    @include bg-container($footer-color);
    min-height: $footer-bottom-height;

    .wrapper {
        @include wrapper(2em, $paddingWrapper);
    }
}

//Content
.footer {
    @include flex(row, space-between, center);
    text-transform: uppercase;
    font-weight: 600;

    //LEFT sign up
    &__signup {
        border: 2px solid $primary-color;
        padding: 1em 1em;
        cursor: pointer;

        a {
            color: white;
        }

        &:hover {
            background-color: darken($primary-color, 30%);
        }
    }

    //RIGHT follow us
    &__social ul {
        @include flex(row, flex-end, center);
        gap: 1.2em;

        span {
            color: $primary-color;
            font-size: 1.2rem;
        }

        a:hover img {
            filter: brightness(180%);
        }
    }
}
</style>