
<template>
    <div class="header">
        <h1>Com todos Molhos</h1>
    </div>

    <div class="loop">
        <div v-for="(obj, index) in todos"
        v-bind:key="obj.id"
        class="todoItem"
        >
       {{ index }} {{ obj.title }}
        </div>
    </div>
</template>

<script>
    export default{
        name: 'cabeca',
        data(){
            return{
                todos: [
                    {
                        "userId":1,
                        "id":1,
                        "title":"Frango",
                        "completed": false
                    },
                    {
                        "userId":1,
                        "id":2,
                        "title":"Mix Picanha",
                        "completed": false
                    },
                    {
                        "userId":1,
                        "id":3,
                        "title":"Carne Bovina",
                        "completed": false
                    },
                    {
                        "userId":1,
                        "id":4,
                        "title":"Carne Suina",
                        "completed": false
                    },
                    {
                        "userId":1,
                        "id":5,
                        "title":"Carne Caprina",
                        "completed": false
                    }
                ]
            }
        }
    }
</script>

<style>
    .todoItem{
        background-color: rgba(0, 42, 24, .5);
        margin: 0 0 5px 0;
        padding: 10px;
    }
    .header{
        background-color: rgba(0, 0, 0, .5);
    }
</style>