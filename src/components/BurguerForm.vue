<template>
    
    <div>
        <p>componente de msg</p>
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
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Salame">
                        <span>Salame</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Cheddar">
                        <span>Cheddar</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="Bacon">
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
        max-width: 400px;
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

</style>
