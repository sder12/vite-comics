<script>
export default {
    name: "FooterBottom"
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <footer>
                <h1>Footer Bottom</h1>
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
</style>