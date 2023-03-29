<script>
import { store } from '../store';
import axios from 'axios';


export default {
    name: 'AppMain',
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
                    console.log(response.data);
                    // this.store.projects = response;
                    // console.log(this.store.projects);   
                });
        }
    },
    created() {
            this.getProjects();
    }
}
</script>

<template>
    <h2>
        Projects
    </h2>
</template>

<style lang="scss" scoped>
</style>