<script>
export default {
    name: "AppHeader",
    data() {
        return {
            nav: [
                {
                    link: "characters",
                    href: "#",
                    active: false,
                },
                {
                    link: "comics",
                    href: "#",
                    active: true,
                },
                {
                    link: "movies",
                    href: "#",
                    active: false,
                },
                {
                    link: "tv",
                    href: "#",
                    active: false,
                },
                {
                    link: "games",
                    href: "#",
                    active: false,
                },
                {
                    link: "collectibles",
                    href: "#",
                    active: false,
                },
                {
                    link: "videos",
                    href: "#",
                    active: false,
                },
                ,
                {
                    link: "fans",
                    href: "#",
                    active: false,
                },
                {
                    link: "news",
                    href: "#",
                    active: false,
                },
                {
                    link: "shop",
                    href: "#",
                    active: false,
                }
            ]
        }
    }
}
</script>

<template>
    <!-- Container-wrapper -->
    <div class="container">
        <div class="wrapper">

            <header class="header">
                <!-- Header logo -->
                <section class="header__logo">
                    <div>
                        <img src="../assets/img/dc-logo.png" alt="">
                    </div>
                </section>
                <!-- Header Nav -->
                <section class="header__navigation">
                    <ul>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                        <li><a href="#">Link</a></li>
                    </ul>
                </section>
            </header>
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container {
    @include bg-container(white);

    .wrapper {
        @include wrapper(.2em, $paddingWrapper);
    }
}

.header {
    height: $header-height;
    @include flex(row, space-between, center);

    &__logo div {
        width: $header-logo;
        height: $header-logo;
    }

    &__navigation ul {
        @include flex(row, flex-end, center);
        gap: 1em;
    }
}
</style>