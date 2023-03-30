<script>
import { store } from '../store';

import axios from 'axios';

import ProjectCard from '../components/ProjectCard.vue';

export default {
    name: 'AppProjects',
    components: {
        ProjectCard
    },
    data () {
        return {
            store,
            projects: []
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
                    console.log(response);
                    return this.store.projects = response.data.data.data;
                });
        }
    },
    created() {
        this.getProjects();
    }
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <h2>
                    All projects
                </h2>
            </div>
        </div>
    </div>
    <div class="container">
        <div class="row g-3 mb-4">
            <!-- Qui cards -->
            <div v-for="project in store.projects" class="col-12 col-sm-4 col-md-3">
                <ProjectCard :project="project" />
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
</style>