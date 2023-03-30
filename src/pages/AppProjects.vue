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
            projects: [],
            project: null
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
                    console.log(response.data.projects.data);
                    return this.store.projects = response.data.projects.data;
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
    <ProjectCard :project="project" />


</template>

<style lang="scss" scoped>
</style>