<script>
    export default{
        data(){
            return{
                poems: [],
            }
        },

        methods: {
            fetchPoems(){
                axios
                .get('https://flynn.boolean.careers/exercises/api/random/sentence')
                .then((response)=>{
                    this.poems.push(response);
                })
            }
        },

        mounted(){
            this.fetchPoems();
        }
    }
</script>

<template></template>

<style></style>