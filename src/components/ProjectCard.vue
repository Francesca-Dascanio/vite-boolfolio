<script>
import { store } from '../store';



export default {
    name: 'ProjectCard',
    props: {
        project: {
            type: Object
        }
    },
    data () {
        return {
            store,
            defaultImg: 'data:image/png;base64,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'
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
                        <img class="card-img-top" :src="project.img ?? defaultImg" alt="Card image cap">
                        <div class="card-body">
                            <h5 class="card-title">
                                {{ project.title }}
                            </h5>
                            <p class="card-text" v-if="project.description ? project.description : '-'">
                                {{ project.description }}
                            </p>
                            <router-link :to="{ name: 'project', params: { slug: project.slug } }" class="btn btn-primary">
                                Single Project
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>