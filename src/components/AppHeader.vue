<script>
import { store } from '../store';


export default {
    name: 'AppHeader',
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
    <header>
        <div class="container">
            <div class="row">
                <div class="col">
                    <h1 class="text-center">
                        Boolfolio
                    </h1>
                    <nav class="navbar navbar-expand-lg navbar-light bg-light">
                        <!-- <a class="navbar-brand" href="#">
                            Home
                        </a> -->
                        <router-link :to="{ name: 'home' }" class="nav-link">
                            Home
                        </router-link>
                        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                            <span class="navbar-toggler-icon"></span>
                        </button>
                        <div class="collapse navbar-collapse" id="navbarNav">
                            <ul class="navbar-nav">
                                <li class="nav-item active">
                                    <!-- <a class="nav-link" href="#">
                                        Projects 
                                        <span class="sr-only">(current)</span>
                                    </a> -->
                                    <router-link :to="{ name: 'projects' }" class="nav-link">
                                        Projects
                                    </router-link>
                                </li>
                                <li class="nav-item active">
                                     <a class="nav-link" href="#">
                                        About me
                                        <span class="sr-only">(current)</span>
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
</style>