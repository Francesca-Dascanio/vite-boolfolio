<script>
import { store } from '../store';


export default {
    name: 'AppHome',
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
                <div class="height d-flex justify-content-center align-items-center">
                    <h2>
                        Il portfolio più bellissimo del mondo
                    </h2>
                </div>
            </div>
        </div>
    </div>

</template>

<style lang="scss" scoped>
    .height {
        height: 500px;
    }
</style>