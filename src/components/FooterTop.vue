<script>
export default {
    name: "FooterTop",
    data() {
        return {
            links: [
                {
                    title: "Dc Comics",
                    subTitle: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "Shop",
                    subTitle: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "DC",
                    subTitle: ["Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
                },
                {
                    title: "Sites",
                    subTitle: ["DC", "MAD Magazines", "DC Kids", "DC Universe", "DC Power Visa"]
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <footer class="footer footer-top">
                <section class="footer__links">
                    <div v-for="(item, index) in links" :key="index">
                        <h4>{{ item.title }}</h4>
                        <ul>
                            <li v-for="(link, index) in item.subTitle" :key="index">
                                <a href="#"> {{ link }}</a>
                            </li>
                        </ul>
                    </div>
                </section>
                <section class="footer__image">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </section>

            </footer>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container {
    @include bg-container(lightGrey);
    background-image: url(../assets/img/footer-bg.jpg);

    .wrapper {
        @include wrapper(0, $paddingWrapper);
    }

    .footer {
        @include flex(row, space-between, center);
        height: $footer-top-height;
        color: white;

        &__links {
            @include flex(row, flex-start, flex-start);
            gap: 1em;
            padding: 2em 0;

            h4 {
                padding-bottom: .8em;
                text-transform: uppercase;
            }

            li {
                padding-bottom: .2rem;

                a {
                    color: $footer-icon-color;
                    font-weight: 400;
                }
            }
        }

        &__image {
            @include flex (row, center, center);
            height: $footer-top-height;
            overflow: hidden;

            img {
                width: calc($footer-top-height + 100px);
            }
        }

    }

}
</style>