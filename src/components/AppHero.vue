<script>
    import AppApi from "./AppApi.vue";
    export default{
        components: { AppApi },
    
        data() {
            return {
                jumboTitle: "Jumbo Title",
            };
        },
        methods: {}
    }
</script>

<template>
    <div class="jumbotron">
        <img src="../assets/jumbo.png" alt="" class="img-fluid">
        <AppApi></AppApi>
    </div>
</template>

<style scoped>
    .jumbotron{
        position: relative;
    }
</style>