<script>
export default {
    name: "MainContent"
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <!-- MAIN -->
            <div>
                <h2>Content goes here</h2>
            </div>
            <!-- / MAIN -->
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;


//Layout
.container {
    @include bg-container($dark-color);

    .wrapper {
        @include wrapper(1em, $paddingWrapper);
    }

}

//Content
//DEBUG
h2 {
    color: white;
}
</style>