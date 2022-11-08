
<script>
import AppHeader from './components/AppHeader.vue';
import MainContent from './components/MainContent.vue';
import MainNav from './components/MainNav.vue';
import FooterTop from './components/FooterTop.vue';
import FooterBottom from './components/FooterBottom.vue';

export default {
    components:
    {
        AppHeader,
        MainContent,
        MainNav,
        FooterTop,
        FooterBottom

    }
}
</script>

<template>

    <AppHeader />
    <MainContent />
    <MainNav />
    <FooterTop />
    <FooterBottom />


</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>