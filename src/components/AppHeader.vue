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
                        <li v-for="(item, index) in nav" :key="index" :class="{ 'active-border': item.active }">
                            <a :href="item.href" :class="{ 'active': item.active }"> {{ item.title }} </a>
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
    @include bg-container(white);

    .wrapper {
        @include wrapper(0em, $paddingWrapper);
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

        li {
            height: $header-height;
            @include flex(row, center, center);
        }

        a {
            font-size: .8rem;
            font-weight: 600;
            text-transform: uppercase;
        }

        .active {
            color: $primary-color;
        }

        .active-border {
            border-bottom: 4px solid $primary-color;
        }
    }
}
</style>