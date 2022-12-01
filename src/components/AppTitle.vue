<script>
    export default{
        data(){
            return{
                title:{
                    mainTitle: "Prima app",
                    subTitle: "con Vite",
                }
            }
        },

        methods: {
            getFullTitle(){
                return this.title.mainTitle + " " + this.title.subTitle;
            }
        }
    }
</script>

<template>
    <h1>{{getFullTitle()}}</h1>
</template>

<style scoped>
    h1{
        padding: 1rem;
        text-align: center;
    }
</style>