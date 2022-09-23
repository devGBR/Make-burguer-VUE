<template>
  <Banner />
  <div class="main-container">
    <h1>Monte o seu burguer:</h1>
    <BurguerForm/>
     
  </div>
</template>

<script>
import Banner from '../components/banner.vue';
import BurguerForm from '@/components/BurguerForm.vue';

export default {
    name: "home",
    components: { Banner, BurguerForm },
   
}
</script>


<style scoped>
 h1{
  
  background-color: #FCBA03;
  
  margin: 0 auto;
  padding: 10px 20px;
  border-radius: 4px;
  font-size: 30px;
  margin-bottom: 10px;
 }
 @media only screen and (max-width:320px){
        h1{
            margin: 0 -40px;
            width: 200px;

        }
    }
    @media only screen and (max-width:375px){
        h1{
          height: 60px;
            padding: 15px 10px;
            
            font-weight: bolder;
            border-radius: 80px ;
            margin-bottom: 10px;
        }
        
    }
    @media only screen and (max-width:426px){
        h1{
        
          height: 60px;
            padding: 15px 10px;
            width: 400px;
            margin: 0 -44.5px;
            font-weight: bolder;
            border-radius: 12px ;
            margin-bottom: 10px;
        }
        
    }
    @media only screen and (min-width:600px){
        h1{
            
          height: 60px;
            padding: 15px 10px;
            width: 400px;
            margin: 0 auto;
            font-weight: bolder;
            border-radius: 12px ;
            margin-bottom: 10px;
            
        }
    }
    @media only screen and (min-width:768px){
        h1{
            
          height: 60px;
            padding: 15px 10px;
            width: 400px;
            margin: 0 auto;
            font-weight: bolder;
            border-radius: 12px ;
            margin-bottom: 10px;
            
        }
    }
    @media only screen and (min-width:1024px){
        h1{
            height: 60px;
            padding: 15px 10px;
            width: 400px;
            margin: 0 auto;
            font-weight: bolder;
            border-radius: 12px ;
            margin-bottom: 10px;
        }
    }
    @media only screen and (min-width:1440px){
        h1{
            width: 420px;
            height: 60px;
            padding: 15px 10px;
            margin: 0 auto;
            margin-bottom: 15px;
            font-weight: bolder;
            border-radius: 12px ;
            
        }
    }
    @media only screen and (min-width:2560px){
      h1{
        width: 800px;
        margin: 0 auto;
        height: 103px;
        padding: 10px 5px;
        font-size: 60px;
        margin-bottom: 20px;
        border-radius: 20px;
            
        }
    }
</style>

