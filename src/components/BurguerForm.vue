<template>
    
    <div>

        <!-- <p>componente de msg</p> -->

        <div>
            <form id="formBurguer" @submit="offload">
                <div class="input-container">
                    <label for="nome">Nome do cliente:</label>
                    <input type="text" id="nome" name="oame" v-model="nome" placeholder="Digite seu nome">
                </div>
                <div class="input-container">
                    <label for="pao">Escolha o pão:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">Selecione o seu pão</option>
                        <option v-for="pao in paes" :key="pao.id" :value="pao.tipo">{{pao.tipo}}</option>
                    </select>
                </div>
                <div class="input-container">
                    <label for="carne">Escolha a carne:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">Selecione o tipo de carne</option>
                        <option v-for="carne in carnes" :key="carne.id" :value="carne.tipo">{{carne.tipo}}</option>
                        
                    </select>
                </div>
                <div id="opcionais-container" class="input-container">
                    <label  for="opcionais" id="opcionais-title">Selecione os opcionais:</label>

                    <div class="checkbox-container" v-for="opcional in opcionaisdata" :key="opcional.id" >
                        <input type="checkbox" name="opcionais" v-model="opcionais" :value="opcional.tipo" id="box">
                        <span>{{opcional.tipo}}</span>
                    </div>
    
                    <div class="input-container">
                        <Button v-on:criarburguer="createBurguer" />
                    </div>
                </div>
            </form>
        </div>
    </div>

</template>

<script>
import Button from './Button.vue';
export default {
    name: "BurguerForm",
    data() {
        return {
            paes: null,
            carnes: null,
            opcionaisdata: null,
            pao: null,
            carne: null,
            opcionais: [],
            msg: null
        };
    },
    methods: {
        async offload(e){
            e.preventDefault();
        },
        async getIngredientes() {
            const req = await fetch("http://localhost:3000/ingredientes");
            const data = await req.json();
            this.paes = data.paes;
            this.carnes = data.carnes;
            this.opcionaisdata = data.opcionais;
        },
        async createBurguer() {
            
            const data = {
                nome: this.nome,
                carne: this.carne,
                pao: this.pao,
                opcionais: Array.from(this.opcionais),
                status: "Solicitado"
            };
            const dataJson = JSON.stringify(data);
            const req = await fetch("http://localhost:3000/burgues", {
                method: "POST",
                headers: { "Content-Type": "application/json" },
                body: dataJson
            });
            const res = await req.json();
            // msg
            //limpa dados
            this.nome = "";
            this.carne = "";
            this.pao = "";
            this.opcionais = "";
        }
    },
    mounted() {
        this.getIngredientes();
    },
    components: { Button }
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
