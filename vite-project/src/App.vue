<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooterTop from './components/AppFooterTop.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';
export default {
    data() {
        return {

        };
    },
    components: {
        AppHeader,
        AppMain,
        AppFooterTop,
        AppFooterBottom
    },  
    methods: {

    }
}
</script>

<template>
    <AppHeader/>
    <AppMain/>
    <AppFooterTop/>
    <AppFooterBottom/>
</template>

<style lang="scss">
@use "assets/scss/main" as *;
@import "assets/scss/partials/reset";
</style>
