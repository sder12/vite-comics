<script>
export default {
    name: "AppHeader",
    data() {
        return {
            nav: [
                {
                    title: "characters",
                    href: "#",
                    active: false,
                },
                {
                    title: "comics",
                    href: "#",
                    active: true,
                },
                {
                    title: "movies",
                    href: "#",
                    active: false,
                },
                {
                    title: "tv",
                    href: "#",
                    active: false,
                },
                {
                    title: "games",
                    href: "#",
                    active: false,
                },
                {
                    title: "collectibles",
                    href: "#",
                    active: false,
                },
                {
                    title: "videos",
                    href: "#",
                    active: false,
                },
                ,
                {
                    title: "fans",
                    href: "#",
                    active: false,
                },
                {
                    title: "news",
                    href: "#",
                    active: false,
                },
                {
                    title: "shop",
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
                        <!-- ERRORE -->
                        <li v-for="(item, index) in nav" :key="index">
                            <a href="#"> {{ item.title }} </a>
                        </li>
                        <!-- FUNZIONA -->
                        <li>
                            <a href="#"> {{ nav[0].title }} </a>
                        </li>
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
    // Debug
    @include bg-container(rgb(187, 187, 187));

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

        a {
            font-size: .8rem;
            text-transform: uppercase;
        }
    }
}
</style>