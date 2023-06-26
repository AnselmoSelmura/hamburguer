<template>
    <div class="form">
        <label>Nome</label>
        <input v-model="name" type="text">
        <br>
        {{ name }}
        <br>
        <label>Senha</label>
        <input v-model="senha" type="password">
        <br>
        {{ senha }}
        <br>
        <br>

        <div class="seleciona">
            <label>Sports</label>
            <select v-model="sports">
                <option value="futebol">Futebol</option>
                <option value="volenbol">Volenbol</option>
                <option value="skate">Skate</option>
                <option value="esgrima">Esgrima</option>
                <option value="Basket">Basket</option>
                <option value="Basebol">Basebol</option>
            </select>
            {{ sports }}
        </div>

<br>

        <div class="activo">
            <label>NewsLetter</label>
            <input type="radio" v-model="newletter" value="Sim">Sim
            <input type="radio" v-model="newletter" value="Não">Não
            {{ newletter }}
        </div>
    </div>
</template>

<script>
    export default{
        name:'formulary',
        data(){
            return{
              name:'AselmoSelmura',
              senha:'122456',
              sports:'fotebol',
              newletter:''
            }
        }
    }
</script>

<style>
    .form{
        color: #fff;
        padding: 20px;
        background-color: green;
    }label{
        padding: 0 10px;
    }.seleciona{
        color: #ff0054;
        background-color: chartreuse;
    }.activo{
        background-color: #ff0054;
    }

</style>