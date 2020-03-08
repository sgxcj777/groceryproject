<template>
  <div>
    <ul>
        <li v-for="item in itemsList" v-bind:key="item.name" v-on:click.self="item.show = !item.show">

            <h2>{{item.name}}</h2>
            <img v-bind:src="item.image" v-show="item.show"/>
                
                
            
        </li>
    </ul>
  </div>
</template>


<script>
export default {
  
  data(){
    return{
        itemsList: [{name:'Marina Bay Sands',image:'./assets/mbs.jpeg',show:false},
                    {name:'Esplanade',image:'./assets/esplanade.jpeg',show:false},
                    {name:'Merlion',image:'./assets/merlion.jpeg',show:false},
                    {name:'Gardens By the Bay',image:'./assets/gardens.jpeg',show:false},
                    {name:'Singapore River',image:'./assets/sg-river.jpg',show:false},
                    {name:'Sentosa',image:'./assets/sentosa.jpeg',show:false}],
        counter: 0
        }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
    background:rgb(122, 63, 100);
    padding:10px;
    border-style: solid;
    border-color:black;
    border-width: 2px;
}
h1{
    color:ivory
}
h2{
  text-align: center
}
#itemsList{
    width: 100%;
    max-width: 1200px;
    margin: 30px auto;
    padding: 0 5px;
    box-sizing: border-box;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 10px;
    border: 1px solid #222;
    margin: 10px;
}
</style>