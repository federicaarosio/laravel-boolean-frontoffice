<script>
    import { RouterView } from 'vue-router';
import AppHeader from './components/AppHeader.vue';

    export default {
    name: "AppVue",
    components: { RouterView, AppHeader }
}
</script>

<template>
    <AppHeader />
    <RouterView />
</template>

<style lang="scss" scoped>

</style>
