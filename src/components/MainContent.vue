<script>
export default {
    name: "MainContent"
}
</script>

<template>

    <!-- BANNER -->
    <div class="banner">
        <span>banner</span>
    </div>

    <!-- CARDS container -->
    <div class="container">
        <div class="wrapper">
            <section class="cards-container">
                <!-- title -->
                <div class="cards-title">
                    <h4>current series</h4>
                </div>
                <!-- cards 6x2 -->
                <div class="cards-wrapper">
                    <span>cards</span>
                </div>
                <!-- button -->
                <div class="cards-button">
                    <button>
                        load more
                    </button>
                </div>
            </section>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;


//Layout
.banner {
    @include bg-container(none);
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
    height: $banner-height;
}

.container {
    @include bg-container($dark-color);

    .wrapper {
        @include wrapper(1em, $paddingWrapper);
        color: white;
    }

}

.cards-container {
    display: flex;
    flex-direction: column;
}

//Content
// cards title
.cards-title {
    align-self: flex-start;

    h4 {
        background-color: $primary-color;
        padding: .5em .5em;
        text-transform: uppercase;
        text-align: center;
    }
}

// cards content
.cards-wrapper {
    align-self: center;
    //DEBUG
    width: 100%;
    height: 100px;
    border: 1px solid white;
}

//cards button
.cards-button {
    align-self: center;

    button {
        background-color: $primary-color;
        color: white;
        padding: .5em 4em;
        text-align: center;
        text-transform: uppercase;
        font-weight: 700;
        font-size: 1rem;
    }
}
</style>