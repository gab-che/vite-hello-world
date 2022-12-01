<script>
    import axios from 'axios'
    export default{
        data(){
            return{
                poems: [],
                counter: 5,
            }
        },

        methods: {
            fetchPoems(){
                axios
                .get('https://flynn.boolean.careers/exercises/api/random/sentence')
                .then((response)=>{
                    this.poems.push(response.data.response);
                })
            },

            generatePoemsArray(){
                for (let i = 0; i < this.counter; i++){
                    this.fetchPoems();
                }
            }
        },

        mounted(){
            this.generatePoemsArray();
        }
    }
</script>

<template>
    <div class="row poems">
        <div class="col-5 m-auto">
            <ul class="list-group">
                <li class="list-group-item"
                    v-for="poem in poems">{{poem}}</li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
    .poems{
        position: absolute;
        top: 20%;
        width: 100%;
    }

    .poems .list-group li{
        background-color: transparent;
        border: none;
        font-style: italic;
        color: white;
    }
</style>