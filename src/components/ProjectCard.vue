<script>
import { store } from '../store';



export default {
    name: 'ProjectCard',
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
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="cards d-flex flex-wrap justify-content-between">
                    <div class="card mb-2" style="width: 18rem;" v-for="project in store.projects">
                        <img class="card-img-top" :src="project.img" alt="Card image cap">
                        <div class="card-body">
                            <h5 class="card-title">
                                {{ project.title }}
                            </h5>
                            <p class="card-text" v-if="project.description ? project.description : '-'">
                                {{ project.description }}
                            </p>
                            <a href="#" class="btn btn-primary">
                                View
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>