<!-- LAYOUT OF ALL OF PAGEs -->
<template>
    <div>
        <Menu />
        <Nuxt />
    </div>
</template>

<script>
import Loader from '@/components/preloader' //Loader component integration
import Menu from '@/components/MainMenu' //Loader component integration


    export default {

        components: { Loader, Menu },

        beforeCreate() {
            this.showHideLoader = true;
        },

        mounted: function() {

        },

        methods: {
            
        },

        data() {
            return {
                showHideLoader: true
            }
        },
    }
</script>

<style></style>