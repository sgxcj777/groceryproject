<template>
  <div class="headerStyle">
    <header>
        <h1>{{ msg }}</h1>
        <nav>
          <ul>
            <li><router-link to="/" exact>List</router-link></li>
            <li><router-link to="/add" exact>Add Item</router-link></li>
          </ul> 
        </nav>
    </header>
    
  </div>
</template>

<script>
export default {
  
  data(){
    return{
        msg: 'Grocery List but actually it is Singapore attractions list hehe :)'
        }
  }
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
</style>