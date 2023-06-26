
<template>
    <div class="header">
        <h1 :classVar="{'title':true, 'title-home':isHome }">
            Com todos Molhos
        </h1>
    </div>

    <p :class="['text', 'title-home']">
        estou tentando começar uma nova fase de promamação, aprendendo novas linguagens e novas formas e ferramentas de programar
    </p>

    <div class="loop">
        <div v-for="(obj, index) in todos"
        v-bind:key="obj.id"
        class="todoItem"
        >
        <img 
            v-bind:src="obj.imgSrc"
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
                pclass: true,
                isHome: true,
                classVar: 'title',
                todos: [
                    {
                        "userId":1,
                        "id":1,
                        "title":"Frango",
                        "completed": false,
                        imgSrc:'https://via.placeholder.com/150'
                    },
                    {
                        "userId":1,
                        "id":2,
                        "title":"Mix Picanha",
                        "completed": false,
                        imgSrc:'https://via.placeholder.com/150'
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
.text{
    color: brown;
}
    .title{
        font-size: 1.5rem;
        color: brown;
    }
    .title-home{
        font-size: 2.5rem;
        color: green;
    }
    .todoItem{
        background-color: rgba(0, 42, 24, .5);
        margin: 0 0 5px 0;
        padding: 10px;
    }
    .header{
        background-color: rgba(0, 0, 0, .5);
    }
</style>