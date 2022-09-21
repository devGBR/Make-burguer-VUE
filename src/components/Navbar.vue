<template>
  <nav>
    <router-link to="/" id="logo-url">
        <img :src="logo" :alt="alt" id="logo">
    </router-link>
   
    <router-link to="/">Home</router-link> 
    |
    <router-link to="/pedidos">Pedidos</router-link>
   
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
    color: #fff;
    
 }
 
 nav #logo-url{
    margin: auto;
    margin-left: 0;
 }
 #logo{
  width: 40px;
  height: 40px;
  
 }
 nav a{
  text-decoration: none;
  color: #FCBA03;
  font-size: 18px;
  margin: 12px;
  transition: .5s; 
 }

 nav a:hover{
   color: #fff; 
 }

</style>