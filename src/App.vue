<script>
import { store } from './store';
import axios from 'axios';

import ProjectCard from './components/ProjectCard.vue';
import AppMain from './components/AppMain.vue';

export default {
    name: 'App',
    components: {
        ProjectCard,
        AppMain
    },
    data () {
        return {
            store
        }
    },
    methods: {
        getProjects: function () {
            // Chiamata all'API da App
            axios
                .get('http://127.0.0.1:8000/api/projects', {
                    params: {

                    }
                })
                .then((response) => {
                    console.log(response.data.data.data.data);
                    return this.store.projects = response.data.data.data.data;
                });
        }
    },
    created() {
        this.getProjects();
    }
}
</script>

<template>

<h1 class="text-center my-3">
    Vite Boolfolio
</h1>

<AppMain />
<ProjectCard />


</template>

<style lang="scss">
// @use './styles/main.scss'

</style>
