<template>
    <div class="listado-juegos">
        <h1>Listado de juegos</h1>
        <u class="ul">
            <li class="li" :style="{color:game.color}" v-for="(game,idx) in gamelist" :key="idx"> <a>{{game.code}}</a> | <a>{{game.name}}</a> | <a>{{game.stock}}</a> | <a>{{game.price}}</a></li>
        </u>
    </div>
</template>

<script>

export default {
    props: {
        gamelist: {
            type: Array,
            default: () => []
        },
    },

}
</script>

<style scoped>
.listado-juegos{
        display: inline-grid;
}
h1{
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    margin-left: 80px;
}
a{
     list-style: none;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    text-decoration: none
    
}
    u.ul{
        
        list-style: none;
        background-color: gray;
        text-decoration: none
        
    } 
    li.li{
        width: 400px;
        padding: 10px;
        text-align: center;
        display: -webkit-box;
    }
</style>