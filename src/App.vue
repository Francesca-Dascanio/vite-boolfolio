<script>
import { store } from './store';


import AppCard from './components/AppCard.vue'
import AppMain from './components/AppMain.vue'

export default {
    name: 'App',
    components: {
        AppCard,
        AppMain
    },
    data () {
        return {
            store
        }
    },
    methods: {
       
    } 
}
</script>

<template>

<h1 class="text-center my-3">
    Vite Boolfolio
</h1>

<AppMain />

</template>

<style lang="scss">
// @use './styles/main.scss'

</style>
