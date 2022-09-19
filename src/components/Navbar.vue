<template>
  <nav>
    <div id="logo-url">
    <router-link to="/" >
        <img :src="logo" :alt="alt" id="logo">
    </router-link>
    </div>
    <div>
    <router-link to="/" class="link">Home</router-link> 
    </div>
    |
    <div>
    <router-link to="/pedidos" class = "link">Pedidos</router-link>
    </div>
  </nav>
</template>
<script>
export default {
    name: 'Navbar',
    props: ["logo", "alt"],
}
</script>
<style scoped>
 nav {
    
    background-color: #222;
    border-bottom: 4px solid #111 ;
    padding: 15px 50px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    color: antiquewhite;
    border-radius: 10px;
    
 }
 nav div{
    padding: 10px;
    
 }
 
 #logo-url{
    margin: auto;
    margin-left: 0;
 }
 #logo{
  width: 40px;
  height: 40px;
  
 }
 .link{
  text-decoration: none;
  color: #fff;
  font-size: 18px;
 }

</style>