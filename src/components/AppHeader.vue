<script>
export default {
    name: "AppHeader"
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <header class="header">
                <section class="header__logo">
                    <div>
                        <img src="../assets/img/dc-logo.png" alt="">
                    </div>
                </section>
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
        @include wrapper();
    }
}

.header {
    height: $header-height;
}
</style>