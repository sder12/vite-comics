<script>
export default {
    name: "FooterTop"
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <h1>Footer Top</h1>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container {
    @include bg-container(lightGrey);
    min-height: $footer-top-height;

    .wrapper {
        @include wrapper(3em, $paddingWrapper);
    }
}
</style>