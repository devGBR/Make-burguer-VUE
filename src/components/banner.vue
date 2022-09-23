<template>
  <div id="main-banner">
    <h1>Make Your Burguer</h1>
  </div>
</template>

<script>
export default {
    name: "Banner",

}
</script>

<style scoped>
    #main-banner {
        position: relative;
        background-image: url('/public/img/burger.png');
        background-position: 0 -200px;
        background-size: cover;
        height: 600px;
        display: flex;
        align-items: center;
        justify-content: flex-start;
    }
    #main-banner h1{
        color: #fff;
        background-color: #222;
        text-align: center;
        padding: 20px 40px;

        font-size: 40px;

    }
    @media only screen and (max-width:320px){
        #main-banner{
            background-position: 0 ;
            height: 200px;
        }
    }
    @media only screen and (max-width:375px){
        #main-banner{
            background-position: 0 ;
            height: 130px;
        }
        
    }
    @media only screen and (max-width:426px){
        #main-banner{
            background-position: 0 ;
            height: 300px;
        }
        #main-banner h1{
            font-size: 15px;
            
        }
        
    }
    @media only screen and (min-width:600px){
        #main-banner{
            background-position: 0 ;
            height: 600px;
        }
    }
    @media only screen and (min-width:768px){
        #main-banner{
            background-position: 0 ;
            height: 600px;
        }
    }
    @media only screen and (min-width:1024px){
        #main-banner{
            background-position: 0 -80px;
            height: 600px;
        }
    }
    @media only screen and (min-width:1333px){
        #main-banner{
            background-position: 0 -170px;
            height: 600px;
        }
    }
    @media only screen and (min-width:1440px){
        #main-banner{
            background-position: 0 -200px;
            height: 600px;
        }
    }
    @media only screen and  (min-width:2560px){
            #main-banner{
                background-position: 0 -360px;
                height: 1080px;
            }
            #main-banner h1{
            color: #fff;
            margin: 60px;
            font-size: 100px;
        }
    }
</style>