<script>
import { store } from './store';

import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';


export default {
    name: 'App',
    components: {
        AppHeader,
        AppFooter
    },
    data () {
        return {
            store
        }
    }
}
</script>

<template>
    <AppHeader />
    <router-view></router-view>
    <AppFooter />
</template>

<style lang="scss">
// @use './styles/main.scss'

</style>
