<script>
import { store } from '../store';


export default {
    name: 'AppProjects',
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
                <!-- Qui cards -->
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
</style>