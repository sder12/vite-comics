<script>
export default {
    name: "MainCard",
    props: {
        cardThumb: String,
        cardPrice: String,
        cardSeries: String,
        cardType: String,
    }
}
</script>

<template>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>
    <div class="card-wrapper">
        <div class="card-img">
            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                alt="">
        </div>
        <div class="card-series">
            Action Comics
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.card-wrapper {
    width: calc(100% / 6);
    @include flex(column, center, center);
    margin-top: 1.5em;
    //DEBUG
    background-color: red;
}

.card-img {
    width: 150px;
    height: 150px;


    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}
</style>