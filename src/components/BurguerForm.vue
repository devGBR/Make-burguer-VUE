<template>
    
    <div>

        <!-- <p>componente de msg</p> -->

        <div>
            <form action="" id="formBurguer">
                <div class="input-container">
                    <label for="nome">Nome do cliente:</label>
                    <input type="text" id="nome" name="oame" v-model="nome" placeholder="Digite seu nome">
                </div>
                <div class="input-container">
                    <label for="pao">Escolha o pão:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">Selecione o seu pão</option>
                        <option value="gergilim">Gergilim</option>
                    </select>
                </div>
                <div class="input-container">
                    <label for="carne">Escolha a carne:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">Selecione o tipo de carne</option>
                        <option value="maminha">Maminha</option>
                        <option value="frango">Frango</option>
                    </select>
                </div>
                <div id="opcionais-container" class="input-container">
                    <label  for="opcionais" id="opcionais-title">Selecione os opcionais:</label>
                    <div class="checkbox-container">


                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Salame" id="box">
                        <span>Salame</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Cheddar" id="box">
                        <span>Cheddar</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Bacon" id="box">

                        <span>Bacon</span>
                    </div>
                    <div class="input-container">
                        <input type="submit" class="submit-btn" value="Criar meu Burguer">
                    </div>
                </div>
            </form>
        </div>
    </div>

</template>

<script>
export default {
    name : "BurguerForm",

}
</script>

<style scoped>
    #formBurguer{
        width: 550px;
        padding: 20px 100px;
        max-width: 500px;

        border: 2px solid #222;

        margin: 0 550px;
    }

    .input-container{
        display: flex;
        flex-direction: column;
        margin-bottom: 20px;
    }

    label{
    font-weight: bold;
    margin-bottom: 15px;
    color: #222;
    padding: 5px 10px;
    border-left-style: solid;
    border-left-color: #FCBA03;
    border-bottom-left-radius: 4px;
    border-top-left-radius: 4px;
    }
    input, select{
        padding: 5px 10px;
        width: 300px;
    }
    #opcionais-container{
        flex-direction: row;
        flex-wrap: wrap;
        
    }
    #opcionais-title{
        width:100%;
    }
    .checkbox-container{
        display: flex;
        align-items: flex-start;
        width: 50%;
        margin-bottom: 20px;
    }

    .checkbox-container span,
    .checkbox-container input{
         width: auto;
    }
    .checkbox-container span{
        margin-left: 6px;
        font-weight: bold;
    }
    .submit-btn{
        background-color: #222;
        color: #FCBA03;
        font-weight: bolder;
        border: 2px solid #222; 
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: 0.5s;
    }
    .submit-btn:hover{
        background-color: transparent;
        color: #222;
    }
    @media only screen and (max-width:320px){
        #formBurguer{
            margin: 0 auto;
            width: 200px;
            padding: 10px 60px;

        }
    }
    @media only screen and (max-width:375px){
        #formBurguer{
            width:400px;
            max-width: 400px;
            margin: 0px -46px;
            padding: 20px 60px;
        }
        
    }
    @media only screen and (max-width:426px){
        #formBurguer{
        max-width: 400px;
        margin: 0px -44.5px;
        padding: 20px 50px;
        }
        
    }
    @media only screen and (min-width:600px){
        #formBurguer{
            max-width: 400px;
            margin: 0 auto;
            padding: 10px 60px;
        }
    }
    @media only screen and (min-width:768px){
        #formBurguer{
            max-width: 400px;
            margin: 0 auto;
            padding: 10px 60px;
        }
    }
    @media only screen and (min-width:1024px){
        #formBurguer{
            max-width: 400px;
            margin: 0 auto;
            padding: 10px 60px;
            
        }
    }
    @media only screen and (min-width:1440px){
        #formBurguer{
            max-width: 420px;
            margin: 0 auto;
            padding: 15px 60px;
            
        }
    }
    @media only screen and (min-width:2560px){
        #formBurguer{
            max-width: 800px;
            width: 800px;
            margin: 0 auto;
            font-size: 80px;
            border: 2px solid #222;
        }
        .submit-btn{
        background-color: #222;
        color: #FCBA03;
        font-weight: bolder;
        border: 2px solid #222; 
        padding: 10px 15px;
        font-size: 40px;
        margin: 0 auto;
        cursor: pointer;
        transition: 0.5s;
        width: 400px;
        height: 140px;
        border-radius: 3%;
    
    }
    #box{
        height: 40px;
        width: 50px;
        
    }
     .input-container{
        padding: 10px;
    
     }
     #pao,#carne,#nome{
        width: 600px;
        height: 100px;
        font-size: 40px;
     }
     #opcionais-container{
        width: 800px;
     }
     .checkbox-container{
        font-size: 50px;
     }
    }
    
    


</style>
