<script>
export default {
    name: "FooterTop",
    data() {
        return {
            //LINKS FOOTER
            //Dc Comics
            comics: {
                title: "Dc Comics",
                subTitle: [
                    {
                        link: "Characters",
                        url: "/characters"
                    },
                    {
                        link: "Comics",
                        url: "/comics"
                    },
                    {
                        link: "Movies",
                        url: "/movie"
                    },
                    {
                        link: "TV",
                        url: "/tv"
                    },
                    {
                        link: "Games",
                        url: "/games"
                    },
                    {
                        link: "Videos",
                        url: "/videos"
                    },
                    {
                        link: "News",
                        url: "/news"
                    }
                ]
            },
            //Shop
            shop: {
                title: "Shop",
                subTitle: [
                    {
                        link: "Shop DC",
                        url: "/shop-dc"
                    },
                    {
                        link: "Shop DC Collectibles",
                        url: "/shop-dc-collectibles"
                    }
                ]
            },
            //DC
            dc: {
                title: "DC",
                subTitle: [
                    {
                        link: "Terms Of Use",
                        url: "/terms-of-use"
                    },
                    {
                        link: "Privacy policy (New)",
                        url: "/privacy-policy"
                    },
                    {
                        link: "Ad Choices",
                        url: "/privacy-policy"
                    },
                    {
                        link: "Advertising",
                        url: "/asvertising"
                    },
                    {
                        link: "Jobs",
                        url: "/jobs"
                    },
                    {
                        link: "Subscriptions",
                        url: "/subscriptions"
                    },
                    {
                        link: "Advertising",
                        url: "/privacy-policy"
                    },
                    //  "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"
                    {
                        link: "Talent Workshops",
                        url: "/talent"
                    },
                    {
                        link: "CPSC Certificates",
                        url: "/Cpsc-certificate"
                    },
                    {
                        link: "Rating",
                        url: "/rating"
                    },
                    {
                        link: "Shop Help",
                        url: "/shop-help"
                    },
                    {
                        link: "Contact Us",
                        url: "/contact-us"
                    }
                ]
            },
            //Sites
            sites: {
                title: "Sites",
                subTitle: [
                    {
                        link: "DC",
                        url: "/dc"
                    },
                    {
                        link: "MAD Magazines",
                        url: "/mad-magazines"
                    },
                    {
                        link: "DC Kids",
                        url: "/dc-kids"
                    },
                    {
                        link: "DC Universe",
                        url: "/dc-universe"
                    }
                    ,
                    {
                        link: "DC Power Visa",
                        url: "/dc-power-visa"
                    }
                ]
            }

        }
    }
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <!-- Footer Top -->
            <footer class="footer">
                <!-- Left - Links -->
                <section class="footer__links">
                    <div>
                        <div>
                            <h4>{{ comics.title }}</h4>
                            <ul>
                                <li v-for="(links, index) in comics.subTitle" :key="index">
                                    <a :href="links.url"> {{ links.link }}</a>
                                </li>
                            </ul>
                        </div>

                        <div class="mt-2">
                            <h4>{{ shop.title }}</h4>
                            <ul>
                                <li v-for="(shops, index) in shop.subTitle" :key="index">
                                    <a :href="shops.url"> {{ shops.link }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div>
                        <h4>{{ dc.title }}</h4>
                        <ul>
                            <li v-for="(dcs, index) in dc.subTitle" :key="index">
                                <a :href="dcs.url"> {{ dcs.link }}</a>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h4>{{ sites.title }}</h4>
                        <ul>
                            <li v-for="(site, index) in sites.subTitle" :key="index">
                                <a :href="site.url"> {{ site.link }}</a>
                            </li>
                        </ul>
                    </div>
                </section>
                <!-- Right - Img -->
                <section class="footer__image">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </section>
            </footer>
            <!-- / Footer Top -->
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

// Layout
.container {
    @include bg-container(lightGrey);
    background-image: url(../assets/img/footer-bg.jpg);

    .wrapper {
        @include wrapper(0, $paddingWrapper);
    }
}

//Content
.mt-2 {
    margin-top: 2em
}

.footer {
    @include flex(row, space-between, center);
    height: $footer-top-height;
    color: white;

    // LEFT links
    &__links {
        @include flex(row, flex-start, flex-start);
        gap: 1em;
        padding: 2em 0;

        & div {
            margin-right: .5em;
        }

        h4 {
            padding-bottom: .8em;
            text-transform: uppercase;
        }

        li {
            padding-bottom: .3rem;
            font-size: .9rem;

            a {
                color: $footer-icon-color;
                font-weight: 400;

                &:hover {
                    color: white;
                }
            }
        }
    }

    //RIGHT img
    &__image {
        @include flex (row, center, center);
        height: $footer-top-height;
        overflow: hidden;

        img {
            width: calc($footer-top-height + 100px);
        }
    }

}
</style>